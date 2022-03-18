<template>
  <div class="ecosystem-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
          <div class="pos-mask">
                <div class="wrap-1">
                <div class="con-1">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold font-white">REIcosystem</h1>
                    <h5 class="font-white font-margin">50 Million $REI Growth Fund For #REIcostystem Building!</h5>
                    <v-btn
                      color="#1D10F8"
                      class="btn-background font-white"
                      width="160"
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
import Explore from '../../components/ecosystem/Explore';
import Process from '../../components/ecosystem/Process';
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
</style>
