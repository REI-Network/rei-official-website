<template>
  <div>
    <v-container class="mt-12">
        <h2>What Dapps You Can Build On REI Network?</h2>
        <v-row class="mt-10" justify="space-between" align="center">
          <v-col cols="12" sm="4">
            <v-hover
                v-slot="{ hover }"
                open-delay="200"
              >
                <v-card
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  color="#EEF3F7"
                  class="dapps"
                  tile
                >
                  <h2>Defi</h2>
                  <div>
                    <img :src="banner" width="90">
                  </div>
                </v-card>
              </v-hover>
              <v-hover
                v-slot="{ hover }"
                open-delay="200"
              >
                <v-card
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  color="#EEF3F7"
                  class="dapps content-bottom"
                  tile
                >
                  <h2>Stablecoin</h2>
                  <div>
                    <img :src="banner1" width="90">
                  </div>
                </v-card>
              </v-hover>
          </v-col>
          <v-col cols="12" sm="4">
            <v-hover
                v-slot="{ hover }"
                open-delay="200"
              >
                <v-card
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  color="#EEF3F7"
                  class="dapps"
                  tile
                >
                  <h2>NFT</h2>
                  <div>
                    <img :src="banner2" width="68">
                  </div>
                </v-card>
              </v-hover>
              <v-hover
                v-slot="{ hover }"
                open-delay="200"
              >
                <v-card
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  color="#EEF3F7"
                  class="dapps content-bottom"
                  tile
                >
                  <h2>Exchange</h2>
                  <div>
                    <img :src="banner3" width="90">
                  </div>
                </v-card>
              </v-hover>
          </v-col>
          <v-col cols="12" sm="4">
            <v-hover
                v-slot="{ hover }"
                open-delay="200"
              >
                <v-card
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  color="#EEF3F7"
                  class="dapps"
                  tile
                >
                  <h2>Gamefi</h2>
                  <div>
                    <img :src="banner4" width="96">
                  </div>
                </v-card>
              </v-hover>
              <v-hover
                v-slot="{ hover }"
                open-delay="200"
              >
                <v-card
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  color="#EEF3F7"
                  class="dapps content-bottom"
                  tile
                >
                  <h2>Socialfi</h2>
                  <div>
                    <img :src="banner5" width="78">
                  </div>
                </v-card>
              </v-hover>
          </v-col>
        </v-row>
         <v-row class="mt-16 learn-join" justify="space-around" align="center">
          <div><v-img :src="bounty" :aspect-ratio="5/6" width="90"/></div>
          <div class="bounty">
            <h3 class="font-gradient">$1,500,000 For Bug Bounty!#REI #Mainnet</h3>
            <p class="font-white">If Ypu Find A Bug Or Have Any Ideas Which Will Improve Mainnet Security.Piz Contact Us</p>
          </div>
          <div class="tow-btn">
            <v-btn
            color="#1D10F8"
            class="btn-background font-white"
            width="120"
            height="36"
           >
              Learn More
          </v-btn>
          <v-btn
            color="green"
            class="btn-background font-white"
            width="120"
            height="36"
           >
              Submit
          </v-btn>
          </div>
        </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      banner: require('@/assets/img/developer/REIiconDefi.png'),
      banner1: require('@/assets/img/developer/Stablecoin.png'),
      banner2: require('@/assets/img/developer/REIiconNFT.png'),
      banner3: require('@/assets/img/developer/exchange.png'),
      banner4: require('@/assets/img/developer/gamefi.png'),
      banner5: require('@/assets/img/developer/REIiconSocialfi.png'),
      bounty:require('@/assets/img/ecosystem/bug bounty.png')
    }
  },
  components: {

  },
}
</script>

<style lang="scss" scoped>
.dapps{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding:20px 40px;

}
.content-bottom{
  margin-top: 20px;
}
.learn-join{
  padding: 20px;
  margin: auto;
  background: linear-gradient(to bottom right, #4B72C8, #9EB8F4);
  .tow-btn{
    display: flex;
    flex-direction: column;
  }
  .btn-background{
    border-radius: 30px;
    cursor: pointer;
    font-weight: 700;
    margin: 4px 0;
  }
}
.font-white{
  color: #FFF;
}
.font-gradient{
  background: linear-gradient(to right, #FFF0B5, #FFADBF);
  -webkit-background-clip: text;
  color: transparent;
}
</style>
