<template>
  <div>
    <v-container class="mt-8 align-item">
        <h2>REI Network Assets</h2>
        <v-row class="mt-10 tools" justify="space-between" align="center">
          <v-col cols="12" md="5" align-self="center" class="left-color">
              <img src="@/assets/img/media/Assets.png" height="280" class="img-style"/>
          </v-col>
          <v-col cols="12" md="7" class="right-color"  align-self="center">
              <h2 class="font-white">Brand Assets</h2>
              <div class="card-text">
               Here Are Official REI.Network Brand Assets And Guidebook
              </div>
                <div style="text-align:right">
                  <v-btn
                  color="#1D10F8"
                  class="btn-background font-white"
                  width="120"
                  height="36"
                  target="_blank"
                  href="https://static.rei.network/media/REI-VIS-Basic-System.zip"
                  depressed
                >
                  Download
                </v-btn>
              </div>
          </v-col>
        </v-row>
        <v-row class="mt-12 learn-join" justify="space-around" align="center">
          <div><v-img :src="banner" :aspect-ratio="6/7" width="120"/></div>
          <div class="bounty">
            <h3 class="font-gradient">Join The REI Network International Community</h3>
            <p class="font-white distance">Join the growing REI.NETWORK community–supporting 13+ languages.</p>
          </div>
          <div class="tow-btn">
            <v-btn
            color="#1D10F8"
            class="btn-background font-white"
            to="/community"
            width="150"
            height="36"
            depressed
           >
              Learn More
          </v-btn>
          </div>
        </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      banner: require('@/assets/img/ecosystem/REIiconDeveloperCommunity.png'),
    }
  },
  components: {

  },
}
</script>

<style lang="scss" scoped>
.align-item{
  max-width: 1220px;
}
.tools{
  background-color:#2A2E3D;
  margin: auto;
  border-radius: 6px;
}
.left-color{
  height:280px;
  padding: 0;
  .img-style{
    width:100%;
    border-radius:6px;
  }
}
.right-color{
  padding:1.2rem 2rem;
  border-radius: 6px;
}
.card-text {
  font-size: 14px;
  color: #FFF;
  margin-top:12px;
}
.btn-background{
  border-radius: 30px;
  margin-top:20px;
}
.learn-join{
  padding: 0 20px;
   margin: auto;
   background: linear-gradient(150deg, #383D4D, #505668);
  .tow-btn{
    margin-top: -20px;
    margin-bottom: 20px;
  }
  .bounty{
     margin-top: 12px;
  }
  .distance{
    margin-top: 20px;
    font-size: 15px;
  }
  .btn-background{
    border-radius: 30px;
    font-size: 12px;
  }
}
.font-white{
  color: #FFF;
}
.font-gradient{
  font-size: 25px;
  font-weight: 900;
  background: linear-gradient(to right, #FFF0B5, #FFADBF);
  -webkit-background-clip: text;
  color: transparent;
}
.learn-join:hover{
  box-shadow: 0 0 20px #ddd;
  transform: translateY(-10px);
  transition: transform .8s;
}
</style>
