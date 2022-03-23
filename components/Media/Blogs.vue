<template>
  <div>
    <v-container class="mt-12">
          <h2>Blogs</h2>
          <h5 class="learn-color">Read More></h5>
          <v-row class="mt-10" justify="space-between">
            <v-col cols="12" md="8" class="">
              <v-carousel v-model="model">
                <v-carousel-item
                  v-for="(item,i) in Lists"
                  :key="i"
                  :src="item.src"
                >
                  </v-carousel-item>
                </v-carousel>
                <v-list three-line style="padding-top:0;">
                    <v-list-item class="list-content">
                      <v-list-item-content>
                        <v-list-item-title>REI|#REIcosystem Started!150 Million $REI Growth Fund For Ecosystem</v-list-item-title>
                        <v-list-item-subtitle class="subtitle-content">We have Witnessed A Lof of Innovative On-Chain Protocols That Have Been Born</v-list-item-subtitle>
                      </v-list-item-content>
                      <v-list-item-action>
                        <v-btn
                          color="#1D10F8"
                          class="font-white"
                          width="120"
                          height="36"
                          tile
                        >
                          Read More
                          </v-btn>
                      </v-list-item-action>
                    </v-list-item>
                  </v-list>
                </v-col>
            <v-col>
              <div class="right-content">
                <v-img :src="banner1" width="100%"  :aspect-ratio="5/4" />
                <div class="cover">
                  REI|#REIcosystem Started!150 Million $REI Growth Fund For Ecosystem Building
                </div>
              </div>
              <div class="right-content">
                <v-img :src="banner1" width="100%"  :aspect-ratio="5/4" style="margin-top:18px"/>
                <div class="cover">
                  REI|#REIcosystem Started!150 Million $REI Growth Fund For Ecosystem Building
                </div>
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
     banner: require('@/assets/img/ecosystem/banner.png'),
      banner1: require('@/assets/img/media/banner.png'),
      banner2: require('@/assets/img/ecosystem/REIiconGame.png'),
      banner3: require('@/assets/img/ecosystem/Stablecoin.png'),
      banner4: require('@/assets/img/ecosystem/NFTMarketplace.png'),
      model: 0,
      Lists: [
          {
            src:require('@/assets/img/ecosystem/banner.png'),
          },
          {
            src:require('@/assets/img/media/banner.png'),
          },
          {
            src:require('@/assets/img/ecosystem/exchange.png'),
          },
          {
            src:require('@/assets/img/ecosystem/banner.png'),
          },
      ],
    }
  },
  components: {

  },
}
</script>

<style lang="scss" scoped>
.learn-color{
  color:#4A37F8;
  text-align: right;
}
.cover-content{
  width: 100%;
  height: 150px;
  background: #D7DBE2;
}
.font-white{
  color: #FFF;
}
.list-content{
  background:#EEF3F7;
  padding:12px 20px;
}
.subtitle-content{
  margin-top: 8px;
}
.right-content{
  position: relative;
  .cover{
    background: #D7DBE2;
    color: #848396;
    padding: 20px;
    position: absolute;
    left: 0;
    bottom: 0;
  }
}
</style>
