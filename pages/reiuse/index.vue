<template>
  <div class="media-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
          <div class="pos-mask">
                <div class="wrap-1">
                  <div class="con-1 typing-text">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold font-white">the REI<br/> network<br/> ecosystem</h1>
                    <h5 class="font-white font-margin">Explore the latest projects on REI network</h5>
                    <v-btn
                      color="#1D10F8"
                      class="btn-background font-white"
                      width="220"
                    >
                      Submit Your Project
                    </v-btn>
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
@keyframes example {
  from{
    transform: translateY(-80px);
  }
  to{
    transform: translateY(0px);
  }
}
</style>
