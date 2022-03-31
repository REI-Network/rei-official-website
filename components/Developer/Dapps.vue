<template>
  <div>
    <v-container class="mt-10 align-item">
        <h1>What Dapps You Can Build On REI Network?</h1>
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
                  <h2>DeFi</h2>
                  <div>
                    <v-img :src="banner" :aspect-ratio="11/10" width="100" />
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
                    <v-img :src="banner1" :aspect-ratio="10/9" width="100" />
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
                    <v-img :src="banner2" :aspect-ratio="4/5" width="80" />
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
                    <v-img :src="banner3" :aspect-ratio="12/11" width="120" />
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
                  <h2>GameFi</h2>
                  <div>
                    <v-img :src="banner4" :aspect-ratio="9/8" width="90" />
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
                  <h2>SocialFi</h2>
                  <div>
                    <v-img :src="banner5" :aspect-ratio="11/12" width="110" />
                  </div>
                </v-card>
              </v-hover>
          </v-col>
        </v-row>
         <v-row class="mt-16 learn-join" justify="space-around" align="center">
          <div><v-img :src="bounty" :aspect-ratio="11/13" width="110" class="img-style"/></div>
          <div class="bounty">
            <h3 class="font-gradient">$1,500,000 For Bug Bounty!#REI #Mainnet</h3>
            <p class="font-white distance">If you find a bug or have any ideas which will improve mainnet security, Please contact us.</p>
          </div>
          <div class="tow-btn">
            <v-btn
            color="#1D10F8"
            class="btn-background font-white"
            href="https://medium.com/@GXS/1-500-000-for-rei-mainnet-bug-bounty-298ad4648146"
            target="_blank"
            width="100"
            height="32"
            depressed
           >
              Learn More
          </v-btn>
          <v-btn
            color="green"
            class="btn-background mt-4 font-white"
            href="https://docs.google.com/forms/d/e/1FAIpQLSdW0tOt5nDVlCZw4auUWW0BrfqxujpV6Y_jJt-ilZsGS4sWOQ/viewform"
            target="_blank"
            width="100"
            height="32"
            depressed
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
.align-item{
  max-width: 1220px;
}
.dapps{
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 158px;
  padding:0 40px;

}
.content-bottom{
  margin-top: 20px;
}
.learn-join{
  margin: auto;
  background: linear-gradient(150deg, #4B72C8, #9EB8F4);
  padding: 0 20px;
  .tow-btn{
    display: flex;
    flex-direction: column;
    margin-bottom: 12px;
  }
  .btn-background{
    border-radius: 30px;
    font-size: 12px;
  }
  .bounty{
     margin-top: 12px;
  }
  .distance{
     margin-top: 20px;
    font-size: 15px;
  }
  .img-style{
    margin-top: 20px;
  }
}
.font-white{
  color: #FFF;
}
.on-hover{
  box-shadow: 0 0 20px #ddd !important;
   transform: translateY(-10px);
  transition: transform .8s;
}
.font-gradient{
  font-size: 25px;
  font-weight: 900;
  background: linear-gradient(90deg, #FFF0B5, #FFADBF);
  -webkit-background-clip: text;
  color: transparent;
}
.learn-join:hover{
  box-shadow: 0 0 20px #ddd !important;
   transform: translateY(-10px);
  transition: transform .8s;

}
</style>
