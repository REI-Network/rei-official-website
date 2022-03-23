<template>
  <div class="media-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
          <div class="pos-mask">
                <div class="wrap-1">
                  <div class="con-1">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold font-white">REI<br/>Media Center<br/> Mainnet Is Now Live!</h1>
                    <h5 class="font-white font-margin">The Latest REI Nnetwork Media Information.</h5>
                  </div>
                </div>
            </div>
      </div>
      <Blogs></Blogs>
  </div>
</template>

<script>
import Blogs from '../../components/Media/Blogs';
export default {
  name: 'MediaPage',
  data() {
    return {
      banner: require('@/assets/img/media/banner.png')
    }
  },
  components:{
    Blogs,
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
</style>
