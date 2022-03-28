<template>
  <div>
    <v-container class="mt-12">
          <h2>Explore REIcostystem</h2>
          <v-row class="mt-4" justify="space-between">
            <v-col cols="12" sm="6">
              <v-hover
                v-slot="{ hover }"
                open-delay="200"
              >
                <v-card
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="card-content"
                  max-width="560"
                  >
                  <div class="img-background">
                    <v-img :src="banner" class="img-style"/>
                  </div>
                  <div class="card-margin">
                    <h3>Decentralized Exchange</h3>
                    <v-card-text class="card-text">
                      Build A Secure,Easy-To-Use Decentralized Exchange On Avalanche.Think Uniswap,0x,And More.
                    </v-card-text>
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
                  class="card-content"
                  max-width="560"
                  >
                  <div class="img-background">
                    <v-img :src="banner3" class="img-style"/>
                  </div>
                  <div class="card-margin">
                    <h3>Stablecoin</h3>
                    <v-card-text class="card-text">
                      Build The Next-Generation Stablecoin On REI Network.Think DAI,USUC And More.
                    </v-card-text>
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
                  class="card-content"
                  max-width="560"
                  >
                  <div class="img-background">
                    <v-img :src="banner3" class="img-style"/>
                  </div>
                  <div class="card-margin">
                    <h3>NFT Marketplace</h3>
                    <v-card-text class="card-text">
                      Gaming And Decentralized Finance(DeFi),Which Also Referred To As Play-To-Earn(P2E)Games.Think Acie
                    </v-card-text>
                  </div>
                </v-card>
              </v-hover>
            </v-col>
            <v-col cols="12" sm="6">
              <v-hover
                v-slot="{ hover }"
                open-delay="200"
              >
                <v-card
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="card-content"
                  max-width="560"

                  >
                  <div class="img-background">
                    <v-img :src="banner1" class="img-style"/>
                  </div>
                  <div class="card-margin">
                    <h3>Lending</h3>
                    <v-card-text class="card-text">
                      Build A Safe,Non-Custodial Lending Solution On Avalanche.Think Compound.Or Aave.
                    </v-card-text>
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
                  class="card-content"
                  max-width="560"
                  >
                  <div class="img-background">
                    <v-img :src="banner2" class="img-style"/>
                  </div>
                  <div class="card-margin">
                    <h3>GameFi</h3>
                    <v-card-text class="card-text">
                      Gaming And Decentralized Finance(DeFi),Which Also Referred To As Play-To-Earn(P2E)Games.Think Acie
                    </v-card-text>
                  </div>
                </v-card>
              </v-hover>
              </v-col>
          </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      banner: require('@/assets/img/ecosystem/exchange.png'),
      banner1: require('@/assets/img/ecosystem/Lending.png'),
      banner2: require('@/assets/img/ecosystem/REIiconGame.png'),
      banner3: require('@/assets/img/ecosystem/Stablecoin.png'),
      banner4: require('@/assets/img/ecosystem/NFTMarketplace.png')
    }
  },
  components: {

  },
}
</script>

<style lang="scss" scoped>
.img-background{
  border-radius: 10px;
  width: 100px;
  height: 100px;
  background: linear-gradient(to bottom, #A2C4FF, #D4FBFC);
}
.img-style{
  float:right;
  margin-right: -10px;
  margin-top: 6px;
}
.card-style{
  // background-color: red;
  display: flex;
  flex-direction: row;
  flex-flow: wrap;
  justify-content: flex-start;
}
.card-content{
  display: flex;
  align-items: center;
  border-radius: 10px;
  padding-left:14px;
  margin-top: 1.6rem;
  .card-margin{
    margin-left: 20px;
    margin-top: 13px;
  }
  h3{
    margin-left: 12px;
  }
}
.card-text {
  margin-top:10px;
  font-size: 14px;
  color: #b1b6bb;
}
</style>
