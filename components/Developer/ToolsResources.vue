<template>
  <div>
    <v-container class="mt-8 align-item">
        <h1>REI Network Tools</h1>
        <v-row class="mt-10 tools" justify="space-between" align="center">
          <v-col cols="12" md="5" align-self="center" class="left-color">
            <v-card
                  tile
                  :elevation="0"
                  color="left-color"
                  >
                  <img src="@/assets/img/developer/REIiconTOOLS.png" height="240" width="250" />
                </v-card>
          </v-col>
          <v-col cols="12" md="7" class="right-color"  align-self="center">
              <h2>REI Explorer</h2>
              <div class="card-text">
                REI Network supports developers to find data on the chain, including transaction records, account information, etc.
              </div>
              <v-btn
              color="#1D10F8"
              class="btn-background font-white"
              href="https://scan.rei.network/"
              target="_blank"
              width="120"
              height="32"
              depressed
            >
              Learn More
            </v-btn>
          </v-col>
        </v-row>
        <h1 class="mt-10">Developer Resources</h1>
        <v-row class="mt-10 tools" justify="space-between" align="center">
          <v-col cols="12" md="5" align-self="center" class="left-color">
            <v-card
                  tile
                  :elevation="0"
                  color="left-color"
                  >
                  <img src="@/assets/img/developer/REIicondoc.png" height="220" width="200" />
                </v-card>
          </v-col>
          <v-col cols="12" md="7" class="right-color"  align-self="center">
              <h2>REI Network Doc</h2>
              <div class="card-text">
                The document provides a detailed interpretation of the concepts, advantages, vision and technical development guidelines of REI Network.
              </div>
              <v-btn
              color="#1D10F8"
              class="btn-background font-white"
              href="https://docs.rei.network/rei-network/welcome-to-rei-network"
              target="_blank"
              width="120"
              height="32"
              depressed
            >
              Learn More
            </v-btn>
          </v-col>
        </v-row>
         <v-row class="mt-12 learn-join" justify="space-around" align="center">
          <div><v-img :src="banner" :aspect-ratio="13/12" width="130"/></div>
          <div class="bounty">
            <h3 class="font-gradient">150 million $REI Growth Fund for #REIcosystem Building! </h3>
            <!-- <p class="font-white distance">If You Find A Bug Or Have Any Ideas Which Will Improve Mainnet Security.Piz Contact Us</p> -->
          </div>
          <div class="tow-btn">
            <v-btn
            color="#1D10F8"
            class="btn-background font-white"
            href="https://medium.com/gxchain-project/rei-reicosystem-started-150-million-rei-growth-fund-for-ecosystem-building-bcb78658e506"
            target="_blank"
            width="120"
            height="36"
            depressed
           >
              Learn More
          </v-btn>
          <v-btn
            color="green"
            class="btn-background font-white"
            href="https://reinetwork0.typeform.com/ApplyforGrants?typeform-source=www.rei.network"
            target="_blank"
            width="120"
            height="36"
            depressed
           >
              Apply
          </v-btn>
          </div>
        </v-row>
        <v-row class="mt-12 learn-join join-rei" justify="space-around" align="center">
          <div><v-img :src="banner1" :aspect-ratio="11/13" width="110" class="img-style"/></div>
          <div class="bounty">
            <h3 class="font-gradient">Join The REI Developer Community</h3>
            <p class="font-white distance">REI’s developer community spans all across the globe. Share your ideas, and build without limits.</p>
          </div>
          <div>
            <v-btn
            color="#1D10F8"
            class="btn-join font-white"
            href="https://discord.com/invite/zhwWkXYtJt"
            target="_blank"
            width="120"
            height="36"
            depressed
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
      banner: require('@/assets/img/community/REIStartanode.png'),
      banner1: require('@/assets/img/ecosystem/REIiconDeveloperCommunity.png'),
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
.tools{
  background-color:#EEF3F7;
  margin: auto;
}
.left-color{
  text-align: center;
  padding: 12px 0;
  background: linear-gradient(180deg, #B5D0FF, #E1FBFC);
}
.right-color{
  padding:1.2rem 2rem;
}
.card-text {
  font-size: 15px;
  color: #8A8A9A;
  margin-top:12px;
}
.img-style{
  margin: 10px 0;
}
.btn-background{
  border-radius: 30px;
  margin-top:20px;
}
.btn-join{
  border-radius: 30px;
}
.learn-join{
  padding: 0 20px;
  margin: auto;
  background: linear-gradient(150deg, #6757A0, #8A7EB5);
  .tow-btn{
    display: flex;
    flex-direction: column;
    margin-bottom: 20px;
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
}
.join-rei{
    background:  linear-gradient(150deg, #383D4D, #505668);
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
.learn-join:hover{
  box-shadow: 0 0 20px #ddd;
  transform: translateY(-10px);
  transition: transform .8s;
}
.tools:hover{
  box-shadow: 0 0 20px #ddd;
  transform: translateY(-10px);
  transition: transform .8s;
}
@media screen and (max-width: 920px){
  .btn-join{
    margin-bottom: 20px;
  }
}
</style>
