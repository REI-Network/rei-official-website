<template>
  <div>
    <v-container class="align-center">
      <v-row
        class="mt-10"
      >
        <v-col cols="12">
          <v-row justify="space-between">
            <h2>Application Process</h2>
            <div class="learn-color">Learn Detail></div>
          </v-row>
          <v-row class="mt-16" justify="space-between">
            <div class="process-block">
              <v-img :src="banner" class="img-style"/>
              <h6>Apply</h6>
            </div>
            <div class="process-block">
              <v-img :src="banner1" class="img-style"/>
              <h6>Evaluation Criteria</h6>
            </div>
            <div class="process-block">
              <v-img :src="banner2" class="img-style"/>
              <h6>Funding Distribution Rules</h6>
            </div>
          </v-row>
        </v-col>
        <div class="mt-16 learn-join learn-rei">
          <div><v-img :src="banner3" class="img-style-learn"/></div>
          <div class="bounty">
            <h3 class="font-gradient">$1,500,000 For Bug Bounty!#REI #Mainnet</h3>
            <p class="font-white">If Ypu Find A Bug Or Have Any Ideas Which Will Improve Mainnet Security.Piz Contact Us</p>
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
        </div>
        <div class="mt-14 learn-join join-rei">
          <div><v-img :src="banner4" class="img-style"/></div>
          <div class="bounty">
            <h3 class="font-gradient">$1,500,000 For Bug Bounty!#REI #Mainnet</h3>
            <p class="font-white">If Ypu Find A Bug Or Have Any Ideas Which Will Improve Mainnet Security.Piz Contact Us</p>
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
          </div>
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
.align-center{
  // background: blue;
}
.learn-color{
  color:#4A37F8 ;
}
.process-block{
  width: 31%;
  height: 25rem;
  background: linear-gradient(to bottom, #A4C6FF, #D2FBFC);
  text-align: center;
  padding-top: 6rem;
  .img-style{
    width: 8rem;
    height: 10rem;
    margin:0 auto;
  }
  h6{
    margin-top: 4rem;
  }
}
.learn-join{
  height: 8rem;
  width: 100%;
  background-color: pink;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background: linear-gradient(to bottom right, #4B72C8, #9EB8F4);
  .img-style{
    width: 6rem;
    height: 8rem;
  }
  .img-style-learn{
    width: 4.6rem;
    height: 6.8rem;
  }
  .tow-btn{
    display: flex;
    flex-direction: column;
  }
  .btn-background{
  background-color: blue;
  border-radius: 30px;
  cursor: pointer;
  font-weight: 700;
  margin: 4px 0;
}
}
.join-rei{
    background: linear-gradient(to bottom right, #373943, #404457);
  }
.font-white{
  color: #FFF;
}
.font-gradient{
  background: linear-gradient(to right, #FFF0B5, #FFADBF);
  -webkit-background-clip: text;
  color: transparent;
}
</style>
