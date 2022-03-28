<template>
  <div>
    <v-container class="mt-8">
        <h2>REI Network Tools</h2>
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
              <h2>REI Network Scan</h2>
              <div class="card-text">
                REI.Network Supports Developers To Find Data On The Chain,Including Transaction Records,Account Information,Etc.
              </div>
              <v-btn
              color="#1D10F8"
              class="btn-background font-white"
              width="100"
              height="32"
            >
              Get Started
            </v-btn>
          </v-col>
        </v-row>
        <h2 class="mt-10">Developer Resources</h2>
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
                The Document Provides A Detailed Interpretation Of The Concepts,Advantages,Vision And Technical Development Guidelines Of REI.Network
              </div>
              <v-btn
              color="#1D10F8"
              class="btn-background font-white"
              width="100"
              height="32"
            >
              Learn More
            </v-btn>
          </v-col>
        </v-row>
         <v-row class="mt-12 learn-join" justify="space-around" align="center">
          <div><v-img :src="banner" :aspect-ratio="13/12" width="130"/></div>
          <div class="bounty">
            <h3 class="font-gradient">50 Million $ REI Growth Fund For #REIcosystem Building!</h3>
            <p class="font-white distance">If You Find A Bug Or Have Any Ideas Which Will Improve Mainnet Security.Piz Contact Us</p>
          </div>
          <div class="tow-btn">
            <v-btn
            color="#1D10F8"
            class="btn-background font-white"
            width="120"
            height="36"
           >
              Learn More
          </v-btn>
          <v-btn
            color="green"
            class="btn-background font-white"
            width="120"
            height="36"
           >
              Submit
          </v-btn>
          </div>
        </v-row>
        <v-row class="mt-12 learn-join join-rei" justify="space-around" align="center">
          <div><v-img :src="banner1" :aspect-ratio="12/13" width="120"/></div>
          <div class="bounty">
            <h3 class="font-gradient">$1,500,000 For Bug Bounty!#REI #Mainnet</h3>
            <p class="font-white distance">REI`s Developer Community Spans All Across The Globe.Share Your Ideas,And Build Without Limits.</p>
          </div>
          <div>
            <v-btn
            color="#1D10F8"
            class="btn-background font-white"
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
      banner: require('@/assets/img/community/REIStartanode.png'),
      banner1: require('@/assets/img/ecosystem/REIiconDeveloperCommunity.png'),
    }
  },
  components: {

  },
}
</script>

<style lang="scss" scoped>
.tools{
  background-color:#EEF3F7;
  margin: auto;
}
.left-color{
  text-align: center;
  padding: 12px 0;
  background: linear-gradient(to bottom, #9EC1FF, #D2FCFC);
}
.right-color{
  padding:1.2rem 2rem;
}
.card-text {
  font-size: 14px;
  color: #b1b6bb;
  margin-top:12px;
}
.btn-background{
  border-radius: 30px;
  margin-top:20px;
}
.learn-join{
  padding: 0 20px;
  margin: auto;
  background: linear-gradient(to bottom right, #3E1D8C, #715FA3);
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
    background: linear-gradient(to bottom right, #373943, #404457);
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
</style>
