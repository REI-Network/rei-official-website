<template>
  <div>
    <v-container class="mt-12 align-item">
          <h2>GameFi Projects</h2>
          <v-row class="mt-12">
            <v-col
              cols="12"
              sm="4"
              class="project-background"
              v-for="n in 9"
              :key="n"
            >
            <!-- v-for="(item,i) in Lists"
              :key="i" -->
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  elevation="0"
                  :class="{ 'on-hover': hover }"
                  >
                  <v-list two-line class="list-item">
                    <v-list-item>
                      <v-list-item-avatar size="80">
                        <v-img src="https://cdn.vuetifyjs.com/images/john.png"></v-img>
                      </v-list-item-avatar>
                      <v-list-item-content>
                        <v-list-item-title class="font-white">Defikindom</v-list-item-title>
                        <v-list-item-subtitle class="subtitle-content font-white">We have Witnessed A Lof of<br/> Innovative On-Chain Protocols <br/>That Have Been Born Been Bor</v-list-item-subtitle>
                        <v-list-item-icon class="right-icon" style="margin-bottom:0;"><v-icon class=" font-white">～</v-icon></v-list-item-icon>
                      </v-list-item-content>
                    </v-list-item>
                  </v-list>
                </v-card>
            </v-hover>
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
      banner4: require('@/assets/img/ecosystem/NFTMarketplace.png'),
      Lists:{

      }
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
.subtitle-content{
  margin-top: 12px;
}
.right-icon{
  display:flex;
  justify-content:flex-end;
  padding-right:30px
}
.list-item{
  background-color:#EEF3F7;
}
.list-item:hover{
  background-color:#2A2E3D;
  transform: translateY(-10px);
  transition: transform .8s;
  .font-white{
    color: #FFF;
  }
}
</style>
