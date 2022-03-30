<template>
  <v-container class="align-item">
     <h2 class="mt-12 start-title">Getting Start On REI.NetWork</h2>
     <v-row class="mt-16" justify="space-between" no-gutters>
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
                    <v-img :src="banner" class="img-style"/>
                    <h6>Start a node</h6>
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
                    <v-img :src="banner1" class="img-style"/>
                    <h6>Become a validator</h6>
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
                    <v-img :src="banner2" class="img-style"/>
                    <h6>Stake for validator</h6>
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
                    <v-img :src="banner3" class="img-style"/>
                    <h6>Stake for Free Gas</h6>
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
                    <v-img :src="banner4" class="img-style"/>
                    <h6>Exchange integration</h6>
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
  // height: 25rem;
  text-align: center;
  padding:3rem 0;
  margin-top: 1.2rem;
  .img-style{
    width: 6rem;
    height: 6rem;
    margin:0 auto;
  }
  h6{
    margin-top: 4rem;
  }
}
.on-hover{
    transform: translateY(-10px);
    transition: transform .8s;
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
