<template>
  <div class="developer-page">
      <div class="pos-r">
          <v-img :src="banner" height="550" />
          <div class="pos-mask">
            <div class="wrap-1">
                <div class="con-1 typing-text">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold font-white">Build<br/>Dapps On<br/>REI.Network</h1>
                    <v-btn
                      color="#1D10F8"
                      class="btn-background font-white"
                      width="160"
                      to="/getStarted"
                      depressed
                    >
                      Get Started
                    </v-btn>
                </div>
            </div>
          </div>
      </div>
      <Reason></Reason>
      <Dapps></Dapps>
      <Compare></Compare>
      <ToolsResources></ToolsResources>
  </div>
</template>

<script>
import Reason from '../../components/Developer/Reason';
import Compare from '../../components/Developer/Compare';
import Dapps from '../../components/Developer/Dapps';
import ToolsResources from '../../components/Developer/ToolsResources';
export default {
  name: 'DeveloperPage',
  data() {
    return {
      banner: require('@/assets/img/developer/banner.png')
    }
  },
  components:{
    Reason,
    Compare,
    Dapps,
    ToolsResources
  }
}
</script>

<style lang="scss" scoped>
.font-white{
  color: #FFF;
}
.btn-background{
  margin-top: 40px;
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
