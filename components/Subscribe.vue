<template>
  <div>
    <v-container class="mt-8">
        <v-row justify="space-between">
          <v-col cols="12" md="6" style="padding-left:0;">
            <h2>Subscribe</h2>
            <div class="left-font mt-2">Subscribe to the newsletter to stay up-to-date with REI Network updates and events.</div>
            <v-col>
              <v-row class="mt-0" justify="space-between" align="center">
                <v-col
                  cols="12"
                  md="9"
                  style="padding-left:0;"
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
                <v-col cols="12" md="3" style="padding-left:0;">
                  <v-btn
                    :loading="loading"
                    color="#1D10F8"
                    class="btn-background"
                    width="120"
                    style="color:white;"
                    @click="subscribe"
                    depressed
                   >
                      Submit
                  </v-btn>
                </v-col>
              </v-row>
            </v-col>
          </v-col>
           <v-col cols="12" md="5">
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
    <v-alert color="rgb(63,163,63)" v-show="successShow" class="sub-success" style="color:#FFF;">
      <v-icon color="#FFF" size="22">{{ mdiCheckCircle }}</v-icon>
      <span class="ml-4">Thank you for subscription.</span>
    </v-alert>
  </div>
</template>
<script>
import { mdiCheckCircle } from '@mdi/js'
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
      mdiCheckCircle,
      banner: require('@/assets/img/ecosystem/exchange.png'),
      banner1: require('@/assets/img/ecosystem/Lending.png'),
      banner2: require('@/assets/img/ecosystem/REIiconGame.png'),
      banner3: require('@/assets/img/ecosystem/Stablecoin.png'),
      banner4: require('@/assets/img/ecosystem/NFTMarketplace.png'),
      links: [
        {
          img:require("../assets/img/icon/Vector.svg"),
          href: "https://github.com/rei-network",
          color: "#4b4b4b",
        },
        {
          img:require("../assets/img/icon/Vector-1.svg"),
          href: "https://twitter.com/GXChainGlobal",
          color: "#60aadb",
        },
        {
          img:require("../assets/img/icon/Vector-2.svg"),
          href: "https://www.reddit.com/r/GXS/",
          color: "#eb443b",
        },
        {
          // href: "https://t.me/GXChain_international",
          icon: "M9.78,18.65L10.06,14.42L17.74,7.5C18.08,7.19 17.67,7.04 17.22,7.31L7.74,13.3L3.64,12C2.76,11.75 2.75,11.14 3.84,10.7L19.81,4.54C20.54,4.21 21.24,4.72 20.96,5.84L18.24,18.65C18.05,19.56 17.5,19.78 16.74,19.36L12.6,16.3L10.61,18.23C10.38,18.46 10.19,18.65 9.78,18.65Z",
          color: "#41a0d7",
          subs: [
            {
              link: "https://t.me/GXChain_international",
              en: "English International Community",
            },
            {
              link: "https://t.me/gxchainkorean",
              en: "Korean Community",
            },
            {
              link: "https://t.me/GXChain_Rus",
              en: "Russian Community",
            },
            {
              link: "https://t.me/GXChainhispano",
              en: "Spanish Community",
            },
            {
              link: "https://t.me/GXChainDeutsch",
              en: "German Community",
            },
            {
              link: "https://t.me/GXChainJapanese",
              en: "Japanese Community",
            },
            {
              link: "https://t.me/GXChainBrazil",
              en: "Brazil Community",
            },
            {
              link: "https://t.me/GXChainItalia",
              en: "Italian Community",
            },
            {
              link: "https://t.me/gxchainvietnam",
              en: "Vietnamese Community",
            },
            {
              link: "https://t.me/GXChainAfrica",
              en: "African Community",
            },
            {
              link: "https://t.me/GXChainTurkey",
              en: "Turkish Community",
            },
            {
              link: "https://t.me/gxchainsrilanka",
              en: "Sri Lanka Community",
            },
            {
              link: "https://t.me/GXChain_Indonesia",
              en: "Indonesian Community",
            },
          ],
        },
        {
          img:require("../assets/img/icon/ri_kakao-talk-fill.svg"),
          color: "#ffc107",
          href: "https://open.kakao.com/o/gghzljsb",
        },
        {
          img:require("../assets/img/icon/Group 82.svg"),
          href: "https://discord.com/invite/zhwWkXYtJt",
          color: "#714bdf",
        },
      ],
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
  color: #8A8A9A;
}
.font-white{
  color: #FFF;
}
.v-text-field input{
  border: none;
}
.sub-success {
  width: 425px;
  padding:12px;
  // height: 43px;
  // line-height: 200px;
  // background: #fff;
  // border: 2px solid #2b85fb;
  // border-radius: 10px;
  // color: #666;
  font-size: 18px;
  text-align: center;
  position: fixed;
  left: 0;
  right: 0;
  bottom:0px;
  margin: auto;
}
</style>
