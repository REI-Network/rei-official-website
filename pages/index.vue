<template>
  <div class="index-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
          <div class="pos-mask">
                <div class="wrap-1">
                <div class="con-1">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold" style="width:200px">{{animatedText}}<span id="caret">&nbsp;</span></h1>
                    <!-- <h1>{{animatedText}}</h1> -->
                </div>
                </div>
            </div>
      </div>
      <div class="index-statistic">
        <v-container>
        <v-row class="white--text text-center">
            <v-col
                cols="12"
                md="4"
                class="d-flex flex-column justify-center"
            >
                <div class="py-4">
                    <h2 class="font-bebas">2,983,713</h2>
                    <p>Total Wallet Addresses</p>
                </div>
            </v-col>
            <v-col
                cols="12"
                md="4"
                class="d-flex flex-column justify-center "
            >
                <div class="py-4 border-both">
                    <h2 class="font-bebas">2,983,713</h2>
                    <p>Total Wallet Addresses</p>
                </div>
            </v-col>
            <v-col
                cols="12"
                md="4"
                class="d-flex flex-column justify-center"
            >
                <div class="py-4">
                    <h2 class="font-bebas">2,983,713</h2>
                    <p>Total Stake (REI)</p>
                </div>
            </v-col>
        </v-row>
        </v-container>
      </div>
      <div id="video" class="section-video">
        <v-container class="content-width">
            <v-row class="video-box lighten-4 cardbg">
                <v-col
                class="d-flex flex-column justify-center"
                cols="12"
                md="6"
                lg="6"
                >
                <div class="pa-10 ">
                    <div class="text-h3  mb-1 font-italic font-weight-bold">Hello,World</div>
                    <div class="text-h6">
                        REI Mainnet Is<br /> Now Live
                    </div>
                    <div>
                        <v-btn
                            href=""
                            dark
                            rounded
                            color="#2340f0"
                            class="font-weight-bold"
                        >
                            Learn More
                        </v-btn>
                    </div>
                </div>
                </v-col>
                <v-col cols="12" md="6" lg="6">
                <video
                    controls
                    preload="meta"
                    class="video-play"
                    src="https://static.rei.network/media/rei-network.mp4"
                ></video>
                </v-col>
            </v-row>
        </v-container>
      </div>
      <div id="feature-wrap">
          <v-container class="content-width">
            <v-row>
                <v-col
                    class="d-flex flex-column justify-center"
                    cols="12"
                    md="6"
                    lg="6"
                >
                <div class="cardbg">
                    <div class="lighten-4 pa-10 pb-1 pr-16">
                        <div class="text-h5 mb-1 font-italic font-weight-bold">
                            <b class="text-h1 font-weight-bold">F</b>ree Gas
                        </div>
                        <p class="text-justify feat-des pr-16">
                            REI Network can achieve free, users are able to complete on-chain transactions with almost zero fees through the innovative design of staking&replacement for on-chain resources.
                        </p>

                    </div>
                    <div class="d-flex justify-end">
                        <v-img :src="featImg1" contain position="right bottom" height="230" class="imgStyle" />
                    </div>
                </div>
                </v-col>
                <v-col cols="12" md="6" lg="6">
                    <div class="cardbg">
                        <div class="lighten-4 pa-10 pb-1 pr-16">
                            <div class="text-h5 mb-1 font-italic font-weight-bold">
                                <b class="text-h1 font-weight-bold">F</b>ast Transactions
                            </div>
                            <p class="text-justify feat-des pr-16">
                                REI.network pays great attention to speed, with an average block time of 3 seconds. Tps reaches 3000+. Under the premise of ensuring decentralization, it will bring users a faster experience.
                            </p>
                        </div>
                        <div class="d-flex justify-end">
                            <v-img :src="featImg2" contain position="right bottom" height="230" class="imgStyle" />
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
                        <div class="text-h4">Developer</div>
                        <p class="text-justify">
                            Read the REI.network document, learn the features of REI.network, look for development resources, and apply for developer growth funds.
                        </p>
                        <div>
                            <v-btn
                                href=""
                                dark
                                rounded
                                color="#2340f0"
                            >
                                Learn More
                            </v-btn>
                        </div>
                    </div>
                </v-col>
                <v-col cols="12" md="6" lg="6">
                    <div class="cardbg lighten-4 pa-15">
                        <div class="text-h4">REI DAO</div>
                        <p class="text-justify">
                            Join REI.DAO to become a validator, vote for the validator to get rewards, Stake gets Free Gas, participate in community governance, and submit proposals.
                        </p>
                        <div>
                            <v-btn
                                href=""
                                dark
                                rounded
                                color="#2340f0"
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
                        <div class="text-h4">Ecosystem</div>
                        <p class="text-justify">
                            REI.Network can be shared and symbiotic with the EVM ecosystem, also supporting the development of Defi, GameFi, and NFT.
                        </p>
                        <div>
                            <v-btn
                                href=""
                                dark
                                rounded
                                color="#2340f0"
                            >
                                Learn More
                            </v-btn>
                        </div>
                    </div>
                </v-col>
                <v-col cols="12" md="6" lg="6">
                    <div class="cardbg lighten-4 pa-15">
                        <div class="text-h4">Media center</div>
                       <p class="text-justify">
                            Learn about REI's latest brand building, operation trends, development progress, etc.
                        </p>
                        <div>
                            <v-btn
                                href=""
                                dark
                                rounded
                                color="#2340f0"
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
                         <v-img :src="communityImg"/>
                </v-col>
                <v-col cols="12" md="8" lg="8">
                    <div class="px-5">
                        <div class="text-h4 font-weight-bold">
                            REI network community
                        </div>
                        <p class="text-justify">
                           REI's community participants are all over the world. You are welcome to join REI.network, share your creativity, ideas, free use and build dapps.Join the growing REI.NETWORK community–supporting 13+ languages.
                        </p>
                        <div>
                            <v-btn
                                href=""
                                dark
                                rounded
                                color="#2340f0"
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
      <Subscribe></Subscribe>
  </div>
</template>

<script>
import RoadMap from '../components/IndexPage/RoadMap';
import Partner from '../components/IndexPage/Partner';
import Subscribe from '../components/Subscribe';

export default {
  name: 'IndexPage',
  components:{
      RoadMap,
      Partner,
      Subscribe
  },
  data() {
    return {
      sloganText: "Rapid Economical Innonative",
      animatedText: "",
      i: 0,
      banner: require('@/assets/img/index/banner-index.png'),
      communityImg: require('@/assets/img/index/index-community.png'),
      featImg1: require('@/assets/img/index/feat-1.png'),
      featImg2: require('@/assets/img/index/feat-2.png'),
    }
  },
  created() {
    setTimeout(() => this.typeWriter(), 1000);
  },
  methods: {
    typeWriter() {
      const speed = 100;
      if (this.i < this.sloganText.length) {
        this.animatedText += this.sloganText.charAt(this.i);
        this.i++;
        setTimeout(this.typeWriter, speed);
      }
    },
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
.index-page{

}
.index-statistic {
    background: url('@/assets/img/index/mid-bg.png') center center no-repeat;
}
.cardbg {
    background-color: #f2f5f8;
}
.feat-des{

}
.text-nowrap {
  white-space: nowrap;
}
.section-video {
  padding: 20px 0;
}
.content-width{
    max-width: 1220px;
  }
.video-play {
  max-width: 1200px;
  width: 100%;
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
  .font-bebas{
    font-family: bebas;
  }
  #caret {
  border-left: 2px solid #000;
  margin-left: 3px;
  animation: blink-caret 1s infinite;
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
</style>
