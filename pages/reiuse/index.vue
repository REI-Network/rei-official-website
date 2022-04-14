<template>
  <div class="media-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" class="img-banner"/>
          <div class="pos-mask mt-16">
                <div class="wrap-1 mt-10">
                  <div class="con-1 typing-text">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold font-line font-white">The REI<br/>Network<br/> Ecosystem</h1>
                    <h5 class="font-white font-margin">Explore the latest projects on REI Network</h5>
                    <!-- <v-btn
                      color="#1D10F8"
                      class="btn-background font-white"
                      width="220"
                      depressed
                    >
                      Submit Your Project
                    </v-btn> -->
                  </div>
                </div>
            </div>
      </div>
      <GameFi></GameFi>
  </div>
</template>

<script>
import GameFi from '../../components/ReiUse/GameFi';
export default {
  name: 'ReiUsePage',
  data() {
    return {
      banner: require('@/assets/img/ReiUse/banner.png')
    }
  },
  components:{
    GameFi
  }
}
</script>

<style lang="scss" scoped>
.font-white{
  color: #FFF;
}
.font-margin{
  margin-top: 30px;
  margin-bottom: 60px;
}
.btn-background{
  padding: 0 50px;
  border-radius: 30px;
  cursor: pointer;
  font-weight: 700;
}
.typing-text{
  animation-name: example;
  animation-duration: 1s;
}
.font-line{
  line-height: 72px;
  width: 500px;
}
@keyframes example {
  from{
    transform: translateY(-80px);
  }
  to{
    transform: translateY(0px);
  }
}
@media screen and (max-width: 920px){
  .font-line{
    font-size: 48px !important;
  }
}
@media screen and (min-width: 1440px){
  .img-banner{
    height: 750px !important;
  }
}
</style>
