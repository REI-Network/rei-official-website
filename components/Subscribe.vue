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
                <v-col cols="12" md="3">
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
           <v-col cols="12" md="4">
          <h2 id="community">Join The Community</h2>
            <div class="mt-6">
              <v-menu
                open-on-hover
                top
                offset-y
                v-for="(it, i) in links"
                :key="i"
              >
                <template v-slot:activator="{ attrs, on }">
                  <v-btn
                    v-bind="attrs"
                    v-on="on"
                    :color="it.color"
                    x-small
                    :href="it.href"
                    target="_blank"
                    class="mt-3 bdrs-100"
                    :class="
                      i == links.length - 1 ? '' : asMobile ? 'mr-6' : 'mr-8'
                    "
                    style="height: 36px;border-radius:30px;"
                  >
                    <img v-if="it.img" :src="it.img" height="18" />
                    <v-icon v-else size="18" color="white">{{ it.icon }}</v-icon>
                  </v-btn>
                </template>
                <v-list v-if="it.subs" max-height="300" dense>
                  <v-list-item
                    link
                    :href="row.link"
                    target="_blank"
                    v-for="(row, j) in it.subs"
                    :key="j"
                  >
                    <v-list-item-title>
                      {{ row.en }}
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-menu>
            </div>
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
  computed: {
    asMobile() {
      return this.$vuetify.breakpoint.smAndDown;
    }
  },
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
      banner4: require('@/assets/img/ecosystem/NFTMarketplace.png'),
      links:[]
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
.align-item{
  max-width: 1220px;
}
.text-field{
  padding-top: 20px;
}
.left-font{
  font-size: 14px;
  color: #b1b6bb;
}
.btn-background{
  margin-top: -30px;
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
