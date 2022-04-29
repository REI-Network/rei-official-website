<template>
  <div class="community-page">
      <div class="pos-r" id="topAnchor">
          <v-img :src="banner" height="550" class="img-banner"/>
          <div class="pos-mask ">
                <div class="wrap-1 ">
                <div class="con-1 typing-text">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold font-white font-line font-line-height">Join<br/>REI Network<br/>Community</h1>
                    <h5 class="font-white font-margin">
                      REI Network community members are around the world. You are<br/> welcome to join our community, share your creativity, ideas, freely<br/> use and build Dapps on REI Network. Join the growing REI Network<br/> community which supports13+ languages
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
  },
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
@media screen and (max-width: 920px){
  .font-line{
    font-size: 48px !important;
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
