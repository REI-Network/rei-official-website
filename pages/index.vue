<template>
  <div class="index-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
          <div class="pos-mask">
                <div class="wrap-1">
                <div class="con-1">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold">Rapid<br> Economical<br> Innonative</h1>
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
                    <h3>2,983,713</h3>
                    <p>Total Wallet Addresses</p>
                </div>
            </v-col>
            <v-col 
                cols="12"
                md="4"
                class="d-flex flex-column justify-center "
            >
                <div class="py-4">
                    <h3>2,983,713</h3>
                    <p>Total Wallet Addresses</p>
                </div>
            </v-col>
            <v-col 
                cols="12"
                md="4"
                class="d-flex flex-column justify-center"
            >
                <div class="py-4 ">
                    <h3>2,983,713</h3>
                    <p>Total Stake (REI)</p>
                </div>
            </v-col>
        </v-row>
        </v-container>
      </div>
      <div id="video" class="section-video">
        <v-container>
            <v-row class="video-box grey lighten-4">
                <v-col
                class="d-flex flex-column justify-center"
                cols="12"
                md="6"
                lg="6"
                >
                <div class="pa-10">
                    <div class="text-h3  mb-1 font-italic font-weight-bold">Hello,World</div>
                    <div class="text-h6">
                        REI Mainnet Is Now Live
                    </div>
                </div>
                </v-col>
                <v-col cols="12" md="6" lg="6">
                <video
                    controls
                    preload="meta"
                    class="video-play"
                    src=""
                ></video>
                </v-col>
            </v-row>
        </v-container>
      </div>
      <div id="feature-wrap">
          <v-container>
            <v-row>
                <v-col
                    class="d-flex flex-column justify-center"
                    cols="12"
                    md="6"
                    lg="6"
                >
                    <div class="grey lighten-4 pa-15">
                        <div class="text-h4 mb-1 font-italic font-weight-bold">
                            <b class="text-h1 font-weight-bold">F</b>ree Gas
                        </div>
                        <p class="text-justify">
                            REI Network can achieve free, users are able to complete on-chain transactions with almost zero fees through the innovative design of staking&replacement for on-chain resources.
                        </p>
                    </div>
                </v-col>
                <v-col cols="12" md="6" lg="6">
                    <div class="grey lighten-4 pa-15">
                        <div class="text-h4 mb-1 font-italic font-weight-bold">
                            <b class="text-h1 font-weight-bold">F</b>ast Transactions
                        </div>
                        <p class="text-justify">
                            REI.network pays great attention to speed, with an average block time of 3 seconds. Tps reaches 3000+. Under the premise of ensuring decentralization, it will bring users a faster experience.
                        </p>
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
                    <div class="grey lighten-4 pa-15">
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
                    <div class="grey lighten-4 pa-15">
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
                    <div class="grey lighten-4 pa-15">
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
                    <div class="grey lighten-4 pa-15">
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
          <v-container>
            <v-row class="grey lighten-4" justify="space-between" align="center" no-gutters>
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
  </div>
</template>

<script>
import RoadMap from '../components/IndexPage/RoadMap';
import Partner from '../components/IndexPage/Partner';

export default {
  name: 'IndexPage',
  components:{
      RoadMap,
      Partner
  },
  data() {
    return {
      banner: require('@/assets/img/index/banner-index.png'),
      communityImg: require('@/assets/img/index/index-community.png')
    }
  },
}
</script>

<style lang="scss">
.index-statistic {
    background: url('@/assets/img/index/mid-bg.png') center center no-repeat;
}
.text-nowrap {
  white-space: nowrap;
}
.section-video {
  padding: 20px 0;
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
</style>
