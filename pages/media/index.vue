<template>
  <div class="media-page">
      <div class="pos-r media-gradient">
          <div class="first"></div>
          <div class="second"></div>
          <div class="third"></div>
          <div class="pos-mask media-content">
                <v-row class="wrap-1" align="center" justify="center">
                  <v-col class="typing-text">
                    <h1 class="mt-8 text-h2 font-italic font-weight-bold font-white ">Media Center<br/> Is Now Live!</h1>
                    <h5 class="font-white font-margin">The Latest REI Network Media Information.</h5>
                  </v-col>
                  <!-- <v-col cols="12" md="5">
                    <video
                    controls
                    preload="meta"
                    class="video-play"
                    src="https://static.rei.network/media/rei-network.mp4"
                ></video>
                  </v-col> -->
                </v-row>
            </div>
      </div>
      <Blogs></Blogs>
      <Assets></Assets>
  </div>
</template>

<script>
import Blogs from '../../components/Media/Blogs';
import Assets from '../../components/Media/Assets';
export default {
  name: 'MediaPage',
  data() {
    return {
      banner: require('@/assets/img/media/banner.png')
    }
  },
  components:{
    Blogs,
    Assets
  }
}
</script>

<style lang="scss" scoped>
.media-gradient{
  width: 100%;
  height: 300px;
  position: relative;
  z-index: 1;
  display: flex;
  justify-content: center;
}
.font-white{
  color: #FFF;
}
.font-margin{
  margin-top: 30px;
  // margin-bottom: 60px;
}
.video-play {
  max-width: 1200px;
  width: 100%;
}
.media-content{
  width: 1220px;
  z-index: 1000;
  position:relative !important;
}
.first,
.second,
.third {
    height: 300px;
    width: 100vw;
}
.first,
.second,
.third {
    position: absolute;
}
.second,
.third {
    opacity: 0;
}
.first {
    animation: first 10s infinite;
    background: linear-gradient(#2340f0, #00a1f0);
    z-index: 10;
}
@keyframes first {
    0% {
        opacity: 1.0;
    }
    10% {
        opacity: 0.8;
    }
    20% {
        opacity: 0.6;
    }
    30% {
        opacity: 0.4;
    }
    // 40% {
    //     opacity: 0.2;
    // }
    // 50% {
    //     opacity: 0.1;
    // }
    // 60% {
    //     opacity: 0.2;
    // }
    70% {
        opacity: 0.4;
    }
    80% {
        opacity: 0.6;
    }
    90% {
        opacity: 0.8;
    }
    100% {
        opacity: 1.0;
    }
}
.second {
    animation: second 10s infinite;
    animation-delay: 2s;
    background: linear-gradient(#19eaa6, #00a1f0);
    z-index: 20;
}
@keyframes second {
    0% {
        opacity: 0;
    }
    10% {
        opacity: 0.2;
    }
    20% {
        opacity: 0.4;
    }
    30% {
        opacity: 0.6;
    }
    40% {
        opacity: 0.8;
    }
    50% {
        opacity: 1.0;
    }
    60% {
        opacity: 0.8;
    }
    70% {
        opacity: 0.6;
    }
    80% {
        opacity: 0.4;
    }
    90% {
        opacity: 0.2;
    }
    100% {
        opacity: 0;
    }
}
.third {
    animation: third 10s infinite;
    animation-delay: 8s;
    background:linear-gradient(#2340f0, #19eaa6);
    z-index: 30;
}
@keyframes third {
    0% {
        opacity: 0;
    }
    10% {
        opacity: 0.2;
    }
    20% {
        opacity: 0.4;
    }
    30% {
        opacity: 0.6;
    }
    40% {
        opacity: 0.8;
    }
    50% {
        opacity: 1.0;
    }
    60% {
        opacity: 0.8;
    }
    70% {
        opacity: 0.6;
    }
    80% {
        opacity: 0.4;
    }
    90% {
        opacity: 0.2;
    }
    100% {
        opacity: 0;
    }
}
.typing-text{
  animation-name: example;
  animation-duration: 1s;
}
@keyframes example {
  from{
    transform: translateY(-80px);
  }
  to{
    transform: translateY(0px);
  }
}
@media screen and (max-width: 960px){
  .media-gradient{
    height:420px;
  }
.first,
.second,
.third {
    height: 420px;
}
}
</style>
