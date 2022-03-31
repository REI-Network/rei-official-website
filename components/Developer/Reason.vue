<template>
  <div>
    <v-container class="mt-12 align-item">
      <v-row justify="space-between" align="center">
        <h1>Why Build On REI Network?</h1>
        <v-btn class="learn-btn" depressed to="/getStarted">Get Started ></v-btn>
      </v-row>
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
                    <img :src="banner" :aspect-ratio="5/6" width="150" class="img-style"/>
                  </div>
                  <h2 class="more-title">More<br/>Compatible</h2>
                  <v-card-text class="card-text">
                    EVM-compatible and Ethereum RPC, seamless migration of Ethereum
                    applications, Ethereum infrastructure can be used directly.
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
                    <img :src="banner1" :aspect-ratio="17/15" width="170" class="img-style"/>
                  </div>
                  <h2 class="more-title">More<br/>Efficient</h2>
                  <v-card-text class="card-text">
                    No Pow, but green based on Dpos + BFT, second-level blocking Is
                    realized. Blocking Is consensus.
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
                    <img :src="banner2" :aspect-ratio="9/8" width="180" class="img-style"/>
                  </div>
                  <h2 class="more-title">More<br/>Economical</h2>
                  <v-card-text class="card-text">
                    REI Network achieves free model, users are able to complete on-chain
                    transactions with almost zero fees through the innovative design of
                    staking & replacement for on-chain resources.
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
                    <img :src="banner3" :aspect-ratio="15/14" width="150" class="img-style"/>
                  </div>
                  <h2 class="more-title">More<br/>Innovative</h2>
                  <v-card-text class="card-text">
                      Abstract consensus module built in cross-chain
                    mechanism, it can be easily integrated to become a
                    chain making tool.
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
                    <img :src="banner4" :aspect-ratio="16/17"  width="160" class="img-style"/>
                  </div>
                    <h2 class="more-title">More<br/>Fast Transactions</h2>
                  <v-card-text class="card-text">
                    REI Network pays great attention to speed. With an average
                    block time of 3 seconds and 3000+ TPS, it bring users
                    a faster experience.
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
                    <img :src="banner5" :aspect-ratio="9/7" width="180" class="img-style"/>
                  </div>
                  <h2 class="more-title">More<br/>Grants</h2>
                  <v-card-text class="card-text">
                    REIcosystem started! 150 million $REI growth fund
                    for ecosystem building.
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
      banner: require('@/assets/img/developer/REIiconMorrCompatible.png'),
      banner1: require('@/assets/img/developer/REIicon4MoreRfficient.png'),
      banner2: require('@/assets/img/developer/REIicon2MoreEconomical.png'),
      banner3: require('@/assets/img/developer/REIicon5MoreInnovative.png'),
      banner4: require('@/assets/img/developer/REIicon3MoreFastTransactions.png'),
      banner5: require('@/assets/img/developer/REIStartanode.png')
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
.v-btn.v-btn--has-bg{
  background-color: transparent;
}
  .learn-btn{
    color:#4A37F8;
    font-weight: 700;
  }

.more-title{
 color: #000;
 margin-left: 16px;
//  font-weight: 900;
//  font-size: 30px;
}
.on-hover{
    box-shadow: 0 0 20px #ddd !important;
    transform: translateY(-10px);
    transition: transform .8s;
  }
.card-text {
  font-size: 15px;
  color: #8A8A9A;
  margin-top: 20px;
}
.why-background{
  padding-bottom: 1.2rem;
  padding-left:2rem;
  padding-right:2rem;
  height: 420px;
}
.img-background{
  width: 100%;
  height: 120px;
  .img-style{
    float:right;
    margin-right: -2.5rem;
    margin-top: -20px;
  }
}
</style>
