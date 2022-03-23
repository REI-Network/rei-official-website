<template>
  <div>
    <v-container class="mt-12">
        <h2>Partners</h2>
        <v-row no-gutters>
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
            img: require("@/assets/img/index/partner/upbit.png"),
            },
            {
            img: require("@/assets/img/index/partner/ic-bithumb.png"),
            },
            {
            img: require("@/assets/img/index/partner/ic-huobi.png"),
            },
            {
            img: require("@/assets/img/index/partner/hitbtc.png"),
            },
            {
            img: require("@/assets/img/index/partner/ic-bittrex.png"),
            },
            {
            img: require("@/assets/img/index/partner/inblockchain.png"),
            },
            {
            img: require("@/assets/img/index/partner/zhenfund.png"),
            },
            {
            img: require("@/assets/img/index/partner/ic-imTokenLogo.svg"),
            },
            {
            img: require("@/assets/img/index/partner/ic-bitpie2.png"),
            },
            {
            img: require("@/assets/img/index/partner/gate.io.png"),
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
      }
  },
  components: {
  },
}
</script>

<style lang="scss" scoped>
.itemTime {
    min-width: 5rem;
}
.img-box {
    display: flex;
    align-items: center;
    max-height: 30px;
    max-width: 60%;
    &:hover {
      box-shadow: 0 0 8px #ddd;
    }
}
</style>
