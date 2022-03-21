<template>
  <div>
    <v-container class="mt-12">
        <h2>Why Build On REI Network?</h2>
        <h5 class="learn-color">Get Start ></h5>
        <v-row justify="space-between">
          <v-col cols="12" sm="4">
            <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="why-background mt-10"
                  color="#EEF3F7"
                  >
                  <div class="img-background">
                    <img :src="banner" height="180" width="180" class="img-style"/>
                  </div>
                  <div class="title">More<br/>Compatible</div>
                  <v-card-text class="card-text">
                    Compatible With EVM And Ethereum RPC Seamless Migration Of Ethereum Applications Ethereum Infrastructure Can Be Used Directly.
                  </v-card-text>
                </v-card>
            </v-hover>
             <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="why-background mt-10"
                  color="#EEF3F7"
                  >
                  <div class="img-background">
                    <img :src="banner1" height="180" width="180" class="img-style"/>
                  </div>
                  <div class="title">More<br/>Efficient</div>
                  <v-card-text class="card-text">
                    No Pow,Green Based On Dpos + BFT,Second Level Block Out Is Realized Block Out Is Consensus.
                  </v-card-text>
                </v-card>
            </v-hover>
          </v-col>
          <v-col cols="12" sm="4">
            <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="why-background mt-10"
                  color="#EEF3F7"
                  >
                  <div class="img-background">
                    <img :src="banner1" height="180" width="180" class="img-style"/>
                  </div>
                  <div class="title">More<br/>Economical</div>
                  <v-card-text class="card-text">
                    REI Network Can Achieve Free,Users Are Able To Complete On-Chain Transparent With Almost Zero Fees Through The Innovative Design Of Staking&Replacement For On-Chain Resources.
                  </v-card-text>
                </v-card>
            </v-hover>
             <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="why-background mt-10"
                  color="#EEF3F7"
                  >
                  <div class="img-background">
                    <img :src="banner3" height="180" width="180" class="img-style"/>
                  </div>
                  <div class="title">More<br/>Innovative</div>
                  <v-card-text class="card-text">
                    Abstract Consensus Module Build In Cross Chain Mechanism It Can Be Easily Combined To Become A Chain Marking Tool.
                  </v-card-text>
                </v-card>
            </v-hover>
          </v-col>
          <v-col cols="12" sm="4">
            <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="why-background mt-10"
                  color="#EEF3F7"
                  >
                  <div class="img-background">
                    <img :src="banner2" height="180" width="180" class="img-style"/>
                  </div>
                    <div class="title">More<br/>Fast Transactions</div>
                  <v-card-text class="card-text">
                    REI.Network Pays Great Attention To Speed,With An Average Block Time Of 3 Seconds-Tips Reachs 3000+.
                    Under The Premise Of Ensuring Decentralization,It Will Bring Users A Faster Experience.
                  </v-card-text>
                </v-card>
            </v-hover>
             <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="why-background mt-10"
                  color="#EEF3F7"
                  >
                  <div class="img-background">
                    <img :src="banner4" height="180" width="180" class="img-style"/>
                  </div>
                  <div class="title">More<br/>Grants</div>
                  <v-card-text class="card-text">
                    REIcosystem Started 150 Million $REI Growth Fund For Ecosystem Building.
                  </v-card-text>
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
.learn-color{
  color:#4A37F8;
  text-align: right;
}
.title{
 color: #000;
 margin-left: 16px;
 font-weight: 700;
 font-size: 36px;
}
.card-text {
  font-size: 14px;
  color: #b1b6bb;
  margin-top: 20px;
}
.why-background{
  padding-bottom: 1.2rem;
  padding-left:2rem;
  padding-right:2rem;
  height: 390px;
}
.img-background{
  width: 100%;
  height: 120px;
  .img-style{
    float:right;
    margin-right: -2.5rem;
    margin-top: -2.5rem;
  }
}
</style>
