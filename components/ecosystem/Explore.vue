<template>
  <div>
    <v-container class="align-center">
      <v-row
        class="mt-10"
      >
        <v-col>
          <h2>Explore REIcostystem</h2>
          <v-row class="mt-10">
            <v-col class="card-style">
              <div class="card-content">
                <div class="img-background">
                  <v-img :src="banner" class="img-style"/>
                </div>
                <div class="card-margin">
                  <h3>Decentralized Exchange</h3>
                  <div class="card-text mt-3">
                    Build A Secure,Easy-To-Use Decentralized Exchange On Avalanche.Think Uniswap,0x,And More.
                  </div>
                </div>
              </div>
              <div class="card-content">
                <div class="img-background">
                  <v-img :src="banner1" class="img-style"/>
                </div>
                <div class="card-margin">
                  <h3>Lending</h3>
                  <div class="card-text mt-3">
                    Build A Safe,Non-Custodial Lending Solution On Avalanche.Think Compound.Or Aave.
                  </div>
                </div>
              </div>
              <div class="card-content">
                <div class="img-background">
                  <v-img :src="banner2" class="img-style"/>
                </div>
                <div class="card-margin">
                  <h3>GameFi</h3>
                  <div class="card-text mt-3">
                    Gaming And Decentralized Finance(DeFi),Which Also Referred To As Play-To-Earn(P2E)Games.Think Acie
                  </div>
                </div>
              </div>
              <div class="card-content">
                <div class="img-background">
                  <v-img :src="banner3" class="img-style"/>
                </div>
                <div class="card-margin">
                  <h3>Stablecoin</h3>
                  <div class="card-text mt-3">
                    Build The Next-Generation Stablecoin On REI Network.Think DAI,USUC And More.
                  </div>
                </div>
              </div>
              <div class="card-content">
                <div class="img-background">
                  <v-img :src="banner4" class="img-style"/>
                </div>
                <div class="card-margin">
                  <h3>NFT Marketplace</h3>
                  <div class="card-text mt-3">
                    Gaming And Decentralized Finance(DeFi),Which Also Referred To As Play-To-Earn(P2E)Games.Think Acie
                  </div>
                </div>
              </div>
            </v-col>
          </v-row>
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
  border-radius: 6px;
  width: 6rem;
  height: 6rem;
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
  width: 46%;
  align-items: center;
  // background-color: pink;
  margin-right: 40px;
  border-radius: 4px;
  padding: 1.2rem 1.6rem;
  .card-margin{
    margin-left: 20px;
  }
}
.card-content:hover{
   box-shadow:rgb(0 0 0 / 10%) 0px 0px 20px;
}

.card-text {
  font-size: 14px;
  color: #b1b6bb;
}
</style>
