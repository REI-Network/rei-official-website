<template>
  <div class="index-page">
      <div class="pos-r" id="topAnchor">
          <v-img :src="banner" height="550" class="img-banner"/>
          <div class="pos-mask">
                <div class="wrap-1">
                <div class="con-1">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold font-line-height">{{animatedText}}<span id="caret">&nbsp;</span></h1>
                </div>
                </div>
            </div>
      </div>
      <div class="index-statistic">
        <v-container class="align-item">
        <v-row class="white--text text-center">
            <v-col
                cols="12"
                md="4"
                class="d-flex flex-column justify-center"
            >
                <div class="py-4">
                    <h2 class="font-bebas">{{stats.totalAddress}}</h2>
                    <p>Total Wallet Addresses</p>
                </div>
            </v-col>
            <v-col
                cols="12"
                md="4"
                class="d-flex flex-column justify-center "
            >
                <div class="py-4 border-both">
                    <h2 class="font-bebas">{{stats.totalTransaction}}</h2>
                    <p>Total Transactions</p>
                </div>
            </v-col>
            <v-col
                cols="12"
                md="4"
                class="d-flex flex-column justify-center"
            >
                <div class="py-4">
                    <h2 class="font-bebas">{{stats.totalStake}}</h2>
                    <p>Total Staked (REI)</p>
                </div>
            </v-col>
        </v-row>
        </v-container>
      </div>
      <div id="video" class="section-video">
        <v-container class="video-container" style="">
            <v-row class="lighten-4" justify="space-between">
              <v-col
                class="d-flex flex-column justify-center"
                cols="12"
                md="5"
                lg="5"
                >
                <div class="font-hello">
                    <div class="mb-1 font-italic font-weight-bold title-size">Hello,World</div>
                    <div class="mainnet font-weight-bold font-italic">
                        REI Mainnet Is Now Live!
                    </div>
                    <!-- <div>
                        <v-btn
                            href=""
                            dark
                            rounded
                            color="#2340f0"
                            class="font-weight-bold mt-8"
                            depressed
                        >
                            Learn More
                        </v-btn>
                    </div> -->
                </div>
                </v-col>
                <v-col cols="12" md="6" class="backdrop-img">
                  <video
                    controls
                    preload="meta"
                    class="video-play"
                    :poster="poster"
                    src="https://static.rei.network/media/rei-network.mp4"
                  >
                  </video>
                </v-col>
            </v-row>
          </v-container>
      </div>
      <Calculation></Calculation>
      <BuiltDapps></BuiltDapps>
      <div id="feature-wrap">
          <v-container class="content-width">
            <v-row>
                <v-col
                    class="d-flex flex-column justify-center"
                    cols="12"
                    md="6"
                    lg="6"
                >
                <div class="cardbg free-fast">
                    <div class="lighten-4 pa-10 pb-1 pr-16">
                        <div class="text-h5 mb-1 font-italic font-weight-bold mt-6">
                            <b class="text-h1 font-weight-bold">F</b>ree Gas
                        </div>
                        <p class="feat-des pr-16 card-text ">
                            REI Network can achieve free gas, users are able to complete on-chain transactions with almost zero fees through the innovative design of staking&replacement for on-chain resources.
                        </p>

                    </div>
                    <div class="d-flex justify-end">
                        <v-img :src="featImg1" contain position="right bottom" height="230" class="imgStyle" />
                    </div>
                </div>
                </v-col>
                <v-col cols="12" md="6" lg="6">
                    <div class="cardbg free-fast" >
                        <div class="lighten-4 pa-10 pb-1 pr-16">
                            <div class="text-h5 mb-1 font-italic font-weight-bold mt-6">
                                <b class="text-h1 font-weight-bold">F</b>ast Transactions
                            </div>
                            <p class="feat-des pr-16 card-text">
                                REI Network pays great attention to speed, with an average block time of 3 seconds. Tps reaches 3000+. Under the premise of ensuring decentralization, it will bring users a faster experience.
                            </p>
                        </div>
                        <div class="d-flex justify-end">
                            <v-img :src="featImg2" contain position="right bottom" height="230" class="imgStyle2" />
                        </div>
                    </div>
                </v-col>
            </v-row>
            <v-row class="">
                <v-col
                class="d-flex flex-column justify-center"
                cols="12"
                md="6"
                lg="6"
                >
                    <div class="cardbg lighten-4 pa-15">
                        <div class="text-h4 font-weight-bold">Developer</div>
                        <p class="card-text mt-4">
                            Read the REI Network document, learn the features of REI Network, look for development resources, and apply for developer growth funds.
                        </p>
                        <div>
                            <v-btn
                                to="/developer"
                                dark
                                rounded
                                color="#2340f0"
                                depressed
                                 class="mt-8"
                            >
                                Learn More
                            </v-btn>
                        </div>
                    </div>
                </v-col>
                <v-col cols="12" md="6" lg="6">
                    <div class="cardbg lighten-4 pa-15">
                        <div class="text-h4 font-weight-bold">REI DAO</div>
                        <p class="card-text mt-4">
                            Join REI DAO to become a validator, vote for the validator to get rewards, staking to get free gas, participate in community governance, and submit proposals.
                        </p>
                        <div>
                            <v-btn
                                href="https://dao.rei.network"
                                target="_blank"
                                dark
                                rounded
                                color="#2340f0"
                                depressed
                                class="mt-8"
                            >
                                Learn More
                            </v-btn>
                        </div>
                    </div>
                </v-col>
            </v-row>
            <v-row class="lighten-4">
                <v-col
                class="d-flex flex-column justify-center"
                cols="12"
                md="6"
                lg="6"
                >
                    <div class="cardbg lighten-4 pa-15">
                        <div class="text-h4 font-weight-bold">REIcosystem</div>
                        <p class="card-text mt-4">
                            REI Network can be shared and symbiotic with the EVM Ecosystem, also supporting the development of Defi, GameFi, and NFT.
                        </p>
                        <div>
                            <v-btn
                                to="/ecosystem"
                                dark
                                rounded
                                color="#2340f0"
                                depressed
                                class="mt-8"
                            >
                                Learn More
                            </v-btn>
                        </div>
                    </div>
                </v-col>
                <v-col cols="12" md="6" lg="6">
                    <div class="cardbg lighten-4 pa-15">
                        <div class="text-h4 font-weight-bold">Media Center</div>
                       <p class="card-text mt-4">
                          Learn about REI Network latest brand building, operation trends, development progress, etc.
                        </p>
                        <div>
                            <v-btn
                                to="/media"
                                dark
                                rounded
                                color="#2340f0"
                                depressed
                                class="mt-8"
                            >
                                Learn More
                            </v-btn>
                        </div>
                    </div>
                </v-col>
            </v-row>
        </v-container>
      </div>
      <div id="index-community">
          <v-container class="content-width">
            <v-row class="cardbg lighten-4" justify="space-between" align="center" no-gutters>
                <v-col
                    align-self="center"
                    cols="12"
                    md="4"
                    lg="4"
                >
                         <v-img :src="communityImg" :aspect-ratio="13/11"/>
                </v-col>
                <v-col cols="12" md="8" lg="8">
                    <div class="px-16 mr-6">
                        <div class="text-h4 mt-4 font-weight-bold">
                            REI Network Community
                        </div>
                        <p class="card-text mt-4">
                          REI Network community members are around the world. You are
                          welcome to join our community, share your creativity, ideas, freely
                          use and build Dapps on REI Network. Join the growing REI Network
                          community which supports 13+ languages.
                        </p>
                        <div>
                            <v-btn
                               to="/community"
                                dark
                                rounded
                                color="#2340f0"
                                depressed
                                class="mt-8 iphone-btn"
                            >
                                Learn More
                            </v-btn>
                        </div>
                    </div>
                </v-col>
            </v-row>
        </v-container>
      </div>
      <RoadMap></RoadMap>
      <Partner></Partner>
  </div>
</template>

<script>
import RoadMap from '../components/IndexPage/RoadMap';
import Partner from '../components/IndexPage/Partner';
import Calculation from '../components/IndexPage/Calculation';
import BuiltDapps from '../components/IndexPage/BuiltDapps';
import Subscribe from '../components/Subscribe';

export default {
  name: 'IndexPage',
  components:{
      RoadMap,
      Partner,
      Subscribe,
      Calculation,
      BuiltDapps
  },
  data() {
    return {
      sloganText: "Rapid Economical Innovative",
      animatedText: "",
      i: 0,
      banner: require('@/assets/img/index/banner-index.png'),
      communityImg: require('@/assets/img/index/index-community.png'),
      featImg1: require('@/assets/img/index/feat-1.png'),
      featImg2: require('@/assets/img/index/feat-2.png'),
      poster:require('@/assets/img/poster.png'),
      stats:{

      }
    }
  },
   watch: {
    animatedText(newV) {
      if (newV === this.sloganText) {
        setTimeout(() => {
          //注意這裡必須使用arrow function才能讓this被正確指向
          this.i = 0;
          this.animatedText = "";
          this.typeWriter();
        }, 6000);
      }
    },
  },

  created() {
    setTimeout(() => this.typeWriter(), 0);
  },
  mounted() {
    this.getData();
  },
  methods: {
    typeWriter() {
      const speed = 200;
      if (this.i < this.sloganText.length) {
        this.animatedText += this.sloganText.charAt(this.i);
        this.i++;
        setTimeout(this.typeWriter, speed);
      }
    },
    async getData(){
        try {
            const { data } = await this.$axios.get('/api/reistats')
            this.stats = data.row.json;
        } catch (error) {
            console.log(error)
        }
    }
  },
}
</script>

<style lang="scss">
  @font-face {
  font-family: 'bebas';
  src: url('../assets/bebas/BEBAS.eot');
  src: url('../assets/bebas/BEBAS.eot#iefix') format('embedded-opentype'),
  url('../assets/bebas/BEBAS.ttf') format('truetype'),
  url('../assets/bebas/BEBAS.woff') format('woff'),
  url('../assets/bebas/BEBAS.svg#Bebas') format('svg');
  font-weight: normal;
  font-style: normal;
}
// .align-item{
//   max-width: 1220px;
// }
.font-bebas{
    font-family: bebas;
  }
.index-page{

}
.index-statistic {
    background: url('@/assets/img/index/mid-bg.png') center center no-repeat;
    background-size:100% 100%;
}
.cardbg {
    background-color: #f2f5f8;
}
.free-fast{
  height:520px
}
.cardbg:hover{
  box-shadow: 0 2px 5px 1px rgb(64 60 67 / 16%) !important;
  transform: translateY(-10px);
  transition: transform .8s;

}
.card-text {
  margin-top:10px;
  font-size: 15px;
  color: #828293;
  line-height: 25px;
}
.mainnet{
  font-size: 36px;
  font-weight: bold;
  color: #828293;
}
.feat-des{

}
.title-size{
  font-size: 80px;
}
.font-hello{
  margin-top:70px;
  max-height: 100px;
}
.text-nowrap {
  white-space: nowrap;
}
.section-video {
  height:760px;
  // margin-top: 12px;
  background: url('@/assets/img/index/home_bg.png') center center no-repeat;
  background-size:1440px 100%;
  background-color: #EEF3F7;
}
.video-container{
  height:760px;
  max-width:1220px;
}
.backdrop-img{
  text-align: center;
  // z-index:1999;
}
.content-width{
    max-width: 1220px;
  }
.video-play {
  max-width: 600px;
  width: 100%;
  border-radius: 20px;
  margin-top: 220px;
  object-fit: cover;
}

 .border-box {
    padding: 0;
    border: 1px solid #fff;
  }
  .win {
    position: relative;
    padding: 0 20px;
  }
  .main {
    max-width: 400px;
    text-align: center;
    margin: 0 auto;
    .main-title {
      font-size: 24px;
      color: #fff;
    }
    .main-text {
      font-size: 18px;
      color: #b1b6bb;
    }
  }
  .border-both{
    border-right: 2px solid #636774;
    border-left: 2px solid #636774;
  }
  #caret {
  border-left: 2px solid #000;
  margin-left: 3px;
  animation: blink-caret 1s infinite;
}
.font-line-height{
  width:200px;
  line-height:100px !important;
}
.calculate-input .theme--light.v-input input, .theme--light.v-input textarea{
  color:#2116E5 !important;
}
.v-slider--horizontal .v-slider__track-container{
  height:10px;
}
@keyframes blink-caret {
  from {
    border-color: transparent;
  }
  to {
    border:none;
    opacity: 0;
  }
}
@media screen and (max-width: 920px){
  .video-container{
      height:560px;
  }
  .section-video{
      height:560px;
      background-image: none;
  }
  .title-size{
    font-size: 30px;
  }
  .mainnet{
    font-size: 20px;
  }
  .index-statistic{
    background-image:none;
    background: #373D4E ;
  }
  .video-play{
    margin-top:50px;
  }
  .free-fast{
    height: 480px;
  }
  .imgStyle{
    height: 0px !important;
  }
  .imgStyle2{
     height: 0px !important;
  }
  .iphone-btn{
    margin-bottom: 40px;
  }
  .border-both{
    border:none;
  }
}
@media screen and (min-width: 1441px){
  .img-banner{
    height: 750px !important;
  }
  .font-line-height{
    margin-top:160px !important;
  }
}
</style>
