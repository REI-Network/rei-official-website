<template>
  <div class="ecosystem-page">
      <div class="pos-r" id="topAnchor">
          <v-img :src="banner" height="550" class="img-banner"/>
          <div class="pos-mask">
                <div class="wrap-1">
                <div class="con-1 typing-text">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold font-white font-line font-line-height">REIcosystem</h1>
                    <h5 class="font-white font-margin">150 Million $REI Growth Fund For #REIcosystem Building!</h5>
                    <v-btn
                      color="#1D10F8"
                      class="btn-background font-white"
                      href="https://form.typeform.com/to/q7cU4ewA"
                      target="_blank"
                      width="160"
                      depressed
                    >
                      Apply
                    </v-btn>
                </div>
                </div>
            </div>
          </div>
          <div>
            <Explore></Explore>
          </div>
          <div>
            <Process></Process>
          </div>
      </div>
</template>

<script>
import Explore from '../../components/Ecosystem/Explore';
import Process from '../../components/Ecosystem/Process';
export default {
  name: 'EcosystemPage',
  data() {
    return {
      banner: require('@/assets/img/ecosystem/banner.png')
    }
  },
  components: {
    Explore,
    Process
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
