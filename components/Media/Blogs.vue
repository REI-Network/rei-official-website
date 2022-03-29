<template>
  <div>
    <v-container class="mt-12 align-item">
          <h2>Blogs</h2>
          <div class="learn-color">
            <v-btn class="learn-btn"
              depressed
              href="https://medium.com/gxchain-project"
              target="_blank"
              >
              Learn Detail>
            </v-btn>
          </div>
          <v-row class="mt-10" justify="space-between">
            <v-col cols="12" md="8" class="">
              <v-card>
                <v-carousel v-model="model">
                <v-carousel-item
                  v-for="(item,i) in Lists"
                  :key="i"
                  :src="item.src"
                >
                  </v-carousel-item>
                </v-carousel>
                <v-list three-line style="padding:0;">
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
              </v-card>
              </v-col>
            <v-col cols="12" md="4">
              <v-card class="right-content">
                <v-img :src="banner1" width="100%"  :aspect-ratio="16/9" />
                <v-list two-line>
                  <v-list-item>
                    <v-list-item-content>
                        <v-list-item-title>REI|#REIcosystem Started!150 Million $REI Growth Fund For Ecosystem</v-list-item-title>
                        <v-list-item-subtitle class="subtitle-content">We have Witnessed A Lof of Innovative On-Chain Protocols That Have Been Born</v-list-item-subtitle>
                      </v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-card>
              <v-card class="right-content">
                <v-img :src="banner1" width="100%"  :aspect-ratio="16/9" style="margin-top:22px"/>
                <v-list two-line>
                  <v-list-item>
                    <v-list-item-content>
                        <v-list-item-title>REI|#REIcosystem Started!150 Million $REI Growth Fund For Ecosystem</v-list-item-title>
                        <v-list-item-subtitle class="subtitle-content">We have Witnessed A Lof of Innovative On-Chain Protocols That Have Been Born</v-list-item-subtitle>
                      </v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-card>
            </v-col>
          </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      banner1: require('@/assets/img/media/banner.png'),
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
.align-item{
  max-width: 1220px;
}
.v-btn.v-btn--has-bg{
  background-color: transparent;
}
.learn-color{
  text-align: right;
  .learn-btn{
    color:#4A37F8;
    font-weight: 700;
  }
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
  padding:12px 20px;
}
.subtitle-content{
  margin-top: 8px;
}
.right-content{
  .cover{
    padding: 20px;
  }
}
</style>

