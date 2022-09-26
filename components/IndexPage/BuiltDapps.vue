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
            <a href="https://dao.rei.network/#/stake" target="_blank"
              >learn more</a
            ></v-btn
          >
        </v-col>
        <v-col cols="12" sm="6" class="all-dapps">
          <div class="explore"></div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  name: "",
  data() {
    return {};
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
  .explore {
    width: 270px;
    height: 70px;
    // background: #1b11f7;
    border-radius: 35px;
    border: 35px solid;
    border-image: linear-gradient(
        171deg,
        rgba(255, 209, 209, 0.5),
        rgba(27, 17, 247, 0.06)
      )
      35 35;
  }
}
</style>
