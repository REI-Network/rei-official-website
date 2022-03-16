<template>
  <div class="index-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
          <div class="pos-mask">
                <div class="wrap-1">
                <div class="con-1">
                    <h1 class="mt-16 text-h2 font-italic font-weight-bold">Rapid<br> Economical<br> Innonative</h1>
                </div>
                </div>
            </div>
      </div>
      <div class="index-statistic">
        <v-row class="white--text text-center">
            <v-col 
                cols="12"
                md="4"
                class="item"
            >
            <h3>2,983,713</h3>
            <p>Total Wallet Addresses</p>

            </v-col>
            <v-col 
                cols="12"
                md="4"
                class="item"
            >
            <h3>2,983,713</h3>
            <p>Total Wallet Addresses</p>

            </v-col>
            <v-col 
                cols="12"
                md="4"
                class="item"
            >
            <h3>2,983,713</h3>
            <p>Total Stake (REI)</p>

            </v-col>
        </v-row>
      </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      banner: require('@/assets/img/index/banner-index.png')
    }
  },
}
</script>

<style lang="scss">
.index-statistic {
    background: url('@/assets/img/index/mid-bg.png') center center no-repeat;
}
</style>
