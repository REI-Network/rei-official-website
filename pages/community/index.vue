<template>
  <div class="community-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
          <div class="pos-mask">
                <div class="wrap-1">
                <div class="con-1 typing-text">
                    <h1 class="mt-12 text-h2 font-italic font-weight-bold font-white">Join<br/>REI Network<br/>Community</h1>
                    <h5 class="font-white font-margin">
                      REI`s Community Participants Are All Over The World.You Are Welcome<br/>To Join ReI.Network,Share Your Creativity,Ideas,Free Use And Build<br/>
                      Dapps.Join The Growing REI.NETWORK Community-Supporting 13+<br/>Languages
                    </h5>
                </div>
                </div>
            </div>
      </div>
      <div>
        <CommunityHub></CommunityHub>
      </div>
  </div>
</template>

<script>
import CommunityHub from '../../components/CommunityHub';
export default {
  name: 'CommunityPage',
  data() {
    return {
      banner: require('@/assets/img/community/banner.png')
    }
  },
  components:{
    CommunityHub,
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
