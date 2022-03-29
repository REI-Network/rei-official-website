<template>
  <div>
    <v-container class="align-center align-item">
          <h2>Application Process</h2>
          <div class="learn-color">
            <v-btn class="learn-btn"
              depressed
              href="https://medium.com/gxchain-project/rei-reicosystem-started-150-million-rei-growth-fund-for-ecosystem-building-bcb78658e506"
              target="_blank"
              >
              Learn Detail>
            </v-btn>
          </div>
          <v-row class="mt-10 apply-rules" justify="space-between">
            <v-col cols="12" sm="4">
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="process-block"
                  >
                  <v-img :src="banner" class="img-style"/>
                  <h6>Apply</h6>
                </v-card>
              </v-hover>
            </v-col>
            <v-col cols="12" sm="4">
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="process-block"
                  >
                  <v-img :src="banner1" class="img-style"/>
                  <h6>Evaluation Criteria</h6>
                </v-card>
            </v-hover>
            </v-col>
            <v-col cols="12" sm="4">
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="process-block"
                  >
                  <v-img :src="banner2" class="img-style"/>
                  <h6>Funding Distribution Rules</h6>
                </v-card>
            </v-hover>
            </v-col>
          </v-row>
        <v-row class="mt-16 learn-join learn-rei" justify="space-around" align="center">
          <div><v-img :src="banner3" :aspect-ratio="11/13" width="110" class="img-style"/></div>
          <div class="bounty">
            <h3 class="font-gradient">$1,500,000 for  Bug Bounty ! #REI #Mainnet</h3>
            <p class="font-white distance">If you find a bug or have any ideas which will improve mainnet security, plz contact us</p>
          </div>
          <div class="tow-btn">
            <!-- <v-btn
            color="#1D10F8"
            class="btn-background font-white"
            width="120"
            height="36"
           >
              Learn More
          </v-btn> -->
          <v-btn
            color="#1D10F8"
            class="btn-background mt-4 font-white"
            href="https://docs.google.com/forms/d/e/1FAIpQLSdW0tOt5nDVlCZw4auUWW0BrfqxujpV6Y_jJt-ilZsGS4sWOQ/viewform"
            target="_blank"
            width="120"
            height="36"
           >
              Submit
          </v-btn>
          </div>
        </v-row>
        <v-row class="mt-14 learn-join join-rei" justify="space-around" align="center">
          <div><v-img :src="banner4" :aspect-ratio="11/13" width="110" class="img-style2"/></div>
          <div class="bounty">
            <h3 class="font-gradient">Join The REI Network Developer Community</h3>
            <p class="font-white distance">REI’s developer community spans all across the globe. Share your ideas, and build without limits.</p>
          </div>
          <div class="tow-btn">
            <v-btn
            color="#1D10F8"
            class="btn-background font-white"
            href="https://discord.com/invite/zhwWkXYtJt"
            target="_blank"
            width="120"
            height="36"
           >
              Join Discord
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
      banner: require('@/assets/img/ecosystem/Apply.png'),
      banner1: require('@/assets/img/ecosystem/DistributionRules.png'),
      banner2: require('@/assets/img/ecosystem/EvaluationCriteria.png'),
      banner3: require('@/assets/img/ecosystem/bug bounty.png'),
      banner4: require('@/assets/img/ecosystem/REIiconDeveloperCommunity.png')
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
.learn-color{
  text-align: right;
  .learn-btn{
    color:#4A37F8;
    font-weight: 700;
  }
}
.on-hover{
    transform: translateY(-10px);
    transition: transform .8s;
  }
.process-block{
  // width: 31%;
  height: 450px;
  background: linear-gradient(180deg, #B5D0FF, #E1FBFC);
  box-shadow: 0px 0px 10px 0px rgba(22, 36, 48, 0.1);
  text-align: center;
  padding-top: 62px;
  padding-bottom:66px;
  .img-style{
    width: 160px;
    height: 200px;
    margin:0 auto;
  }
  h6{
    margin-top: 100px;
  }
}
.learn-join{
  margin: auto;
  background: linear-gradient(to bottom right, #4B72C8, #9EB8F4);
  padding: 0 20px;
  .tow-btn{
    display: flex;
    flex-direction: column;
    margin-bottom: 12px;
  }
  .img-style{
    margin-top: 20px;
  }
  .img-style2{
    margin: 12px 0;
  }
   .bounty{
     margin-top: 12px;
  }
  .distance{
    margin-top: 20px;
    font-size: 15px;
  }
  .btn-background{
    border-radius: 30px;
    font-size: 12px;
  }
}
.join-rei{
    background: linear-gradient(150deg, #383D4D, #505668);
  }
.font-white{
  color: #FFF;
}
.font-gradient{
  font-size: 25px;
  font-weight: 900;
  background: linear-gradient(to right, #FFF0B5, #FFADBF);
  -webkit-background-clip: text;
  color: transparent;
}
@media screen {

}
</style>
