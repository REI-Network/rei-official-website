<template>
  <div>
    <v-container class="mt-12">
      <h2>SubScribe</h2>
        <v-row class="mt-10" justify="space-between">
          <v-col cols="12" md="5">
            <div class="left-font">Subscribe ToThe Newsletter To Stay Up-To-Date With<br/>REI Network Updates And Events.</div>
          </v-col>
          <v-col cols="12" md="6">
            <v-row justify="space-between" align="center">
              <v-col
                cols="12"
                md="9"
                style="height:76px"
              >
                <v-text-field
                  label="Outlined"
                  outlined
                  placeholder="Placeholder"
                ></v-text-field>
              </v-col>
                <v-col cols="12"
                md="3">
                  <v-btn
                  color="#1D10F8"
                  class="btn-background font-white"
                  width="120"
                  height="36"
                >
                  Submit
                </v-btn>
                </v-col>
            </v-row>
          </v-col>
        </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      banner: require('@/assets/img/ecosystem/exchange.png'),
      banner1: require('@/assets/img/ecosystem/Lending.png'),
      banner2: require('@/assets/img/ecosystem/REIiconGame.png'),
      banner3: require('@/assets/img/ecosystem/Stablecoin.png'),
      banner4: require('@/assets/img/ecosystem/NFTMarketplace.png')
    }
  },
  components: {

  },
}
</script>

<style lang="scss" scoped>
.left-font{
  font-size: 14px;
  color: #b1b6bb;
}
.font-white{
  color: #FFF;

}
.right-content{

}
.v-text-field input{
  border: none;
}
</style>
