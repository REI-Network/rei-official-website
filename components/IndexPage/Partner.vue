<template>
  <div style="width: 100%">
    <v-container class="mt-12 content-width">
      <h1>Partners</h1>
      <v-row no-gutters class="mt-12">
        <v-col
          v-for="item in list"
          :key="item.title"
          cols="3"
          md="3"
          lg="2"
          xl="2"
          class="my-4 d-flex justify-center"
        >
          <div class="img-box">
            <v-img contain :src="item.img" max-height="35"> </v-img>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      list: [
        {
          img: require("@/assets/img/index/partner/ic-binance.png"),
        },
        {
          img: require("@/assets/img/index/partner/binance-futures.png"),
        },
        {
          img: require("@/assets/img/index/partner/upbit.png"),
        },
        {
          img: require("@/assets/img/index/partner/bithumb.png"),
        },
        {
          img: require("@/assets/img/index/partner/bitget.png"),
        },
        {
          img: require("@/assets/img/index/partner/gate.png"),
        },
        {
          img: require("@/assets/img/index/partner/binanced-earn.png"),
        },
        {
          img: require("@/assets/img/index/partner/htx.png"),
        },
        {
          img: require("@/assets/img/index/partner/ic-imTokenLogo.svg"),
        },
        {
          img: require("@/assets/img/index/partner/ic-bitpie2.png"),
        },
        {
          img: require("@/assets/img/index/partner/metamask.png"),
        },
        {
          img: require("@/assets/img/index/partner/ic-hiperpay.png"),
        },
        {
          img: require("@/assets/img/index/partner/slowmist.png"),
        },
        {
          img: require("@/assets/img/index/partner/tokocrypto.png"),
        },
        {
          img: require("@/assets/img/index/partner/ic-certik2.png"),
        },
        {
          img: require("@/assets/img/index/partner/ic-perk.png"),
        },
        {
          img: require("@/assets/img/index/partner/grandshare.png"),
        },
        {
          img: require("@/assets/img/index/partner/ic-fenbushi.png"),
        },
        {
          img: require("@/assets/img/index/partner/zhenfund.png"),
        },
        {
          img: require("@/assets/img/index/partner/inblockchain.png"),
        },
        {
          img: require("@/assets/img/index/partner/ic-8dec.png"),
        },
        {
          img: require("@/assets/img/index/partner/ic-linkvc-2.png"),
        },
        {
          img: require("@/assets/img/index/partner/ic-bixin.png"),
        },
        {
          img: require("@/assets/img/index/partner/fission.png"),
        },
        {
          img: require("@/assets/img/index/partner/img.png"),
        },
        {
          img: require("@/assets/img/index/partner/ic-stars-c.png"),
        },
        {
          img: require("@/assets/img/index/partner/yahoo.png"),
        },
        {
          img: require("@/assets/img/index/partner/bloomberg.png"),
        },
        {
          img: require("@/assets/img/index/partner/nasdaq.png"),
        },
        {
          img: require("@/assets/img/index/partner/coin-telegraph.png"),
        },
        {
          img: require("@/assets/img/index/partner/reuters.png"),
        },
        {
          img: require("@/assets/img/index/partner/market-watch.png"),
        },
        {
          img: require("@/assets/img/index/partner/indigo.png"),
        },
      ],
    };
  },
  components: {},
};
</script>

<style lang="scss" scoped>
.itemTime {
  min-width: 5rem;
}
.img-box {
  display: flex;
  align-items: center;
  height: 70px;
  border-radius: 6px;
  border: 1px solid #f0f0f0;
  padding: 12px;
  width: 80%;
  &:hover {
    box-shadow: 0 0 8px #ddd;
  }
}

.content-width {
  max-width: 1220px;
}
</style>
