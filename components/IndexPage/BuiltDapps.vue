<template>
  <div>
    <v-container class="stake-container">
      <v-row justify="space-between" class="dapps">
        <v-col cols="12" sm="6">
          <div class="stake-text">
            There are already hundreds <br />
            of Dapps built on the <br />REI Network
          </div>
          <div class="font-grey dapp-text">
            REI Network Realize lower resource consumption through <br />the
            design of tokenomics.Provides a more user-friendly<br />
            solution.
          </div>
          <v-btn class="more-btn">
            <a href="" target="_blank">learn more</a>
          </v-btn>
        </v-col>
        <v-col cols="12" sm="6" class="all-dapps">
          <div class="explore">
            <v-btn class="explore-btn">
            <a href="" target="_blank">Explore all dApps</a>
          </v-btn>
          </div>
          <v-row class="logo-two">
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo1" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo2" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo3" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo4" width="80" height="80" />
              </div>
            </v-col>
          </v-row>
          <v-row justify="space-around">
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo5" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo6" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo7" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo8" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo1" width="80" height="80" />
              </div>
            </v-col>
          </v-row>
           <v-row class="logo-two">
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo1" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo2" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo3" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo4" width="80" height="80" />
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo5" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo6" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo7" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo8" width="80" height="80" />
              </div>
            </v-col>
            <v-col>
              <div class="img-back">
                <v-img class="image" :src="logo1" width="80" height="80" />
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  name: "",
  data() {
    return {
      logo1: require("../../assets/img/logo/logo_1.jpg"),
      logo2: require("../../assets/img/logo/logo_2.jpg"),
      logo3: require("../../assets/img/logo/logo_3.jpg"),
      logo4: require("../../assets/img/logo/logo_4.png"),
      logo5: require("../../assets/img/logo/logo_5.png"),
      logo6: require("../../assets/img/logo/logo_6.png"),
      logo7: require("../../assets/img/logo/logo_7.jpeg"),
      logo8: require("../../assets/img/logo/logo_8.jpeg"),
    };
  },
  components: {},
  watch: {},
  computed: {},
  mounted() {},
  methods: {},
};
</script>

<style scoped lang="scss">
.stake-container {
  // height: 760px;
  max-width: 1220px;
}
.font-grey {
  color: #7e7e7e;
}
a {
  color: #fff;
  text-decoration: none;
}
.dapps {
  border-radius: 4px;
  background-color: #f2f5f8;
  margin: 12px 0px 0px 0px;
  padding: 60px 40px;
  .stake-text {
    font-size: 32px;
    font-weight: bolder;
  }
  .dapp-text {
    margin-top: 16px;
  }
  .more-btn {
    background-color: blue;
    color: #fff;
    border-radius: 20px;
    margin: 28px 0;
  }
}
.all-dapps {
  border-radius: 8px;
  background-color: #fff;
  padding: 20px;
  position: relative;
  .explore {
    // width: 270px;
    // height: 70px;
    border-radius: 35px;
    background: linear-gradient(171deg,rgba(255, 209, 209, 0.5),rgba(239,237,255));
    position: absolute;
    top: 148px;
    left: 160px;
    z-index: 9;
  }
  .explore-btn {
    background-color: blue;
    color: #fff;
    border-radius: 20px;
    padding: 20px;
    margin: 20px 28px;
  }
  .logo-two{
    .img-back{
      margin:0 15px;
    }
  }
  .img-back {
    width: 80px;
    height: 80px;
    border-radius: 50px;
    box-shadow: 0 0 20px #ddd;
    .image {
      border-radius: 50px;
    }
  }
  .image:hover{
    border: 1px blue solid;
    cursor: pointer;
  }
}
</style>
