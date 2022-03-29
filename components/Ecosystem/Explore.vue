<template>
  <div>
    <v-container class="mt-12 align-item">
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
                      Build a secure, easy-to-use decentralized exchange on Avalanche. Think Uniswap, 0x, and more.
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
                    <h3>Gamefi </h3>
                    <v-card-text class="card-text">
                      Gaming and decentralized finance (DeFi), which also referred to as play-to-earn (P2E) games. Think Axie
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
                      Gaming and decentralized finance (DeFi), which also referred to as play-to-earn (P2E) games. Think Axie
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
                      Build a safe, non-custodial lending solution on Avalanche. Think Compound, or Aave.
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
                    <h3>Stablecoin</h3>
                    <v-card-text class="card-text">
                      Build the next-generation stablecoin on REI Network. Think DAI, USDC and more.
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
.align-item{
  max-width: 1220px;
}
.img-background{
  border-radius: 10px;
  width: 100px;
  height: 100px;
  background: linear-gradient(180deg, #B5D0FF, #E1FBFC);
}
.on-hover{
    transform: translateY(-10px);
    transition: transform .8s;
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
