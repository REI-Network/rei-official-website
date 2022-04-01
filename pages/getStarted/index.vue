<template>
  <v-container class="align-item">
     <h1 class="mt-12 start-title">Getting Start On REI NetWork</h1>
     <v-row class="mt-12 bottom-margin" justify="space-between" no-gutters>
          <v-col cols="12" md="2">
            <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <a href="https://docs.rei.network/developer/quick-start" target="_blank">
                  <v-card tile
                    :elevation="hover ? 12 : 0"
                    :class="{ 'on-hover': hover }"
                    class="process-block node"
                    >
                    <div class="img-style">
                      <v-img :src="banner" :aspect-ratio="10/9" width="100"/>
                    </div>
                    <h4>Start a node</h4>
                  </v-card>
                </a>
              </v-hover>
          </v-col>
          <v-col cols="12" md="2">
            <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <a href="https://docs.rei.network/rei-dao/guides/become-a-validator" target="_blank">
                  <v-card tile
                    :elevation="hover ? 12 : 0"
                    :class="{ 'on-hover': hover }"
                    class="process-block become"
                    >
                    <div class="img-style">
                      <v-img :src="banner1" :aspect-ratio="1" width="90"/>
                    </div>
                    <h4>Become a validator</h4>
                  </v-card>
                </a>
              </v-hover>
          </v-col>
          <v-col cols="12" md="2">
            <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <a href="https://docs.rei.network/rei-dao/guides/voting-for-a-validator" target="_blank">
                  <v-card tile
                    :elevation="hover ? 12 : 0"
                    :class="{ 'on-hover': hover }"
                    class="process-block stake"
                  >
                    <div class="img-style">
                      <v-img :src="banner2" :aspect-ratio="1" width="100"/>
                    </div>
                    <h4>Stake for validator</h4>
                  </v-card>
                </a>
              </v-hover>
          </v-col>
          <v-col cols="12" md="2">
            <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <a href="https://docs.rei.network/rei-dao/guides/stake-for-free-gas" target="_blank">
                  <v-card tile
                    :elevation="hover ? 12 : 0"
                    :class="{ 'on-hover': hover }"
                    class="process-block free-gas"
                  >
                    <div class="img-style">
                      <v-img :src="banner3" :aspect-ratio="11/9" width="110"/>
                    </div>
                    <h4>Stake for Free Gas</h4>
                  </v-card>
                </a>
              </v-hover>
          </v-col>
          <v-col cols="12" md="2">
            <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <a href="https://docs.rei.network/rei-dao/guides/exchange-integration" target="_blank">
                  <v-card tile
                    :elevation="hover ? 12 : 0"
                    :class="{ 'on-hover': hover }"
                    class="process-block exchange"
                    >
                    <div class="img-style">
                      <v-img :src="banner4"  :aspect-ratio="9/10" width="90"/>
                    </div>
                    <h4>Exchange integration</h4>
                  </v-card>
                </a>
              </v-hover>
          </v-col>
        </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'getStarted',
  data() {
    return {
      banner: require('@/assets/img/getStarted/REIStartanode.png'),
      banner1: require('@/assets/img/getStarted/REIBecomeavalidator.png'),
      banner2: require('@/assets/img/getStarted/REIStakeforvalidator.png'),
      banner3: require('@/assets/img/getStarted/REIStakeforFreeGas.png'),
      banner4: require('@/assets/img/getStarted/REIExchangeintegration.png'),
    }
  },
}
</script>

<style lang="scss" scoped>
a{
  text-decoration: none;
}
a:hover{
  text-decoration: underline;
  color: #000;
}
.align-item{
  max-width: 1220px;
}
.start-title{
  text-align: center;
}
.process-block{
  height: 260px;
  text-align: center;
  padding:3rem 0;
  margin-top: 1.2rem;
  .img-style{
    height: 110px;
    width: 100px;
    margin: 0 auto;
  }
  h4{
    margin-top:28px;
  }
}
.on-hover{
  box-shadow: 0 0 20px #ddd !important;
    transform: translateY(-10px);
    transition: transform .8s;
  }
  .bottom-margin{
    margin-bottom: 30px;
  }
.node{
    background: linear-gradient(to bottom, #B7E1F7, #DFF6FF);
  }
  .become{
    background: linear-gradient(to bottom, #C0C4E5, #D6DFF8);
  }
  .stake{
    background: linear-gradient(to bottom, #FFB69D, #FFD0BF);
  }
  .free-gas{
    background: linear-gradient(to bottom, #FFE5AF, #FEEAC9);
  }
  .exchange{
    background: linear-gradient(to bottom, #B8BABA, #E0E0E0);
  }
</style>
