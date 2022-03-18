<template>
  <div>
    <v-container class="align-center">
      <v-row
        class="mt-10"
      >
        <v-col>
          <h2>SubScribe</h2>
          <v-row class="mt-10">
            <v-col class="card-style">

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
</style>
