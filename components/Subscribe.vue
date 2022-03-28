<template>
  <div>
    <v-container class="mt-12">
      <h2>Subscribe</h2>
        <v-row class="mt-10" justify="space-between">
          <v-col cols="12" md="5">
            <div class="left-font">Subscribe To The Newsletter To Stay Up-To-Date With<br/>REI Network Updates And Events.</div>
          </v-col>
          <v-col cols="12" md="6">
            <v-row justify="space-between" align="center">
              <v-col
                cols="12"
                md="9"
                
              >
                <v-text-field
                  v-model="email"
                  type="email"
                  dense
                  hide-details
                  outlined
                  placeholder="Your email address"
                ></v-text-field>
              </v-col>
                <v-col cols="12"
                md="3">
                  <v-btn
                  :loading="loading"
                  color="#1D10F8"
                  class="btn-background font-white"
                  width="120"
                  @click="subscribe"
                >
                  Submit
                </v-btn>
                </v-col>
            </v-row>
          </v-col>
        </v-row>
    </v-container>
    <div v-show="successShow" class="sub-success">
      <v-icon color="#2B85FB" size="64">{{ mdiEmoticonHappyOutline }}</v-icon>
      <span class="ml-4">Thank you for subscription.</span>
    </div>
  </div>
</template>
<script>
import { mdiEmoticonHappyOutline } from '@mdi/js'
export default {
  data() {
    return {
      email: '',
      loading: false,
      disabled: true,
      successShow: false,
      mdiEmoticonHappyOutline,
      banner: require('@/assets/img/ecosystem/exchange.png'),
      banner1: require('@/assets/img/ecosystem/Lending.png'),
      banner2: require('@/assets/img/ecosystem/REIiconGame.png'),
      banner3: require('@/assets/img/ecosystem/Stablecoin.png'),
      banner4: require('@/assets/img/ecosystem/NFTMarketplace.png')
    }
  },
  methods: {
    async subscribe() {
      if(!this.email) return;
      this.loading = true;
      try {
        const resp = await this.$axios.get(
          `https://gateway.rei.network/subscribe?mail=${this.email}`
        )
        // eslint-disable-next-line no-console
        // console.log(resp.data)
        if (resp.data.message) {
          if (resp.data.message === 'success') {
            this.successShow = true
            setTimeout(() => {
              this.successShow = false
            }, 3000)
          } else {
            this.$dialog.error({
              text: resp.data.data || 'Subscribe failed',
              title: 'Error',
            })
          }
        } else {
          this.$dialog.error({
            text: 'Subscribe failed',
            title: 'Error',
          })
        }
      } catch (ex) {
        this.$dialog.error({
          text: ex.message,
          title: 'Error',
        })
      } finally {
        this.loading = false
      }
    },
  },
  components: {

  },
}
</script>

<style lang="scss" scoped>
.left-font{
  font-size: 14px;
  color: #b1b6bb;
}
.font-white{
  color: #FFF;

}
.v-text-field input{
  border: none;
}
.sub-success {
  width: 600px;
  height: 200px;
  line-height: 200px;
  background: #fff;
  border: 2px solid #2b85fb;
  border-radius: 10px;
  color: #666;
  font-size: 18px;
  text-align: center;
  position: fixed;
  left: 0;
  right: 0;
  top: 120px;
  margin: auto;
}
</style>
