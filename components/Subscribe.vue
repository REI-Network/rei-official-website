<template>
  <div>
<<<<<<< Updated upstream
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
                
=======
    <v-container class="mt-12 align-item">
        <v-row class="mt-10" justify="space-between">
          <v-col cols="12" md="6" align-self="flex-end">
            <h2>SubScribe</h2>
            <div class="left-font">Subscribe ToThe Newsletter To Stay Up-To-Date With<br/>REI Network Updates And Events.</div>
            <v-row justify="space-between" align="center" style="margin-top:20px">
              <v-col
                cols="12"
                md="9"
>>>>>>> Stashed changes
              >
                <v-text-field
                  v-model="email"
                  type="email"
                  dense
                  hide-details
                  outlined
<<<<<<< Updated upstream
                  placeholder="Your email address"
=======
                  placeholder="Placeholder"
                  dense
                  class="text-field"
>>>>>>> Stashed changes
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
    },
    disabled() {
      return !this.$regMap.email.test(this.email);
    },
  },
  data() {
    return {
<<<<<<< Updated upstream
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
=======
      email: "",
      links: [
        {
          icon: "mdi-github",
          href: "https://github.com/rei-network",
          color: "#4b4b4b",
        },
        {
          icon: "mdi-twitter",
          href: "https://twitter.com/GXChainGlobal",
          color: "#60aadb",
        },
        {
          icon: "mdi-reddit",
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
        // {
        //   icon: "M12,0 C5.3671875,0 0,5.3671875 0,12 C0,18.6328125 5.3671875,24 12,24 C18.6328125,24 24,18.6328125 24,12 C24,5.3671875 18.6328125,0 12,0 Z M9.2953125,17.7140625 L9.2953125,17.7140625 L9.2953125,17.7140625 L5.1046875,15.6609375 C5.0625,15.61875 4.9734375,15.5296875 4.9734375,15.440625 L4.9734375,5.934375 L9.2484375,8.071875 L9.2484375,17.7140625 L9.2953125,17.7140625 Z M9.8203125,13.1765625 L9.8203125,8.859375 L13.659375,15.0984375 L9.8203125,13.1765625 Z M11.521875,10.6453125 L14.4890625,5.8875 L18.8109375,8.0671875 L14.3578125,15.2671875 L11.521875,10.6453125 Z M18.9375,17.7140625 L18.9375,17.7140625 L18.9375,17.7140625 L14.746875,15.6609375 L18.9375,8.859375 L18.9375,17.7140625 Z",
        //   href: "https://4everland.medium.com/",
        //   color: "#4b4b4b",
        // },
        {
          img: "img/icon/kakao-talk.svg",
          color: "#ffc107",
          href: "https://open.kakao.com/o/gghzljsb",
        },
        {
          icon: "mdi-discord",
          href: "https://discord.com/invite/zhwWkXYtJt",
          color: "#714bdf",
        },
      ],
    };
>>>>>>> Stashed changes
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
