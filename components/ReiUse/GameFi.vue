<template>
  <div>
    <v-container class="mt-12 align-item">
          <h1>Projects</h1>
          <v-row class="mt-8">
            <v-col
              cols="12"
              sm="4"
              class="project-background"
              v-for="(item,i) in lists"
              :key="i"
            >
            <!-- v-for="(item,i) in Lists"
              :key="i" -->
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  elevation="0"
                  :class="{ 'on-hover': hover }"
                  >
                  <v-list two-line class="list-item">
                    <v-list-item>
                      <v-list-item-avatar size="80">
                        <v-img :src="item.logo"></v-img>
                      </v-list-item-avatar>
                      <v-list-item-content>
                        <v-list-item-title class="font-white"><h3>{{item.app_name}}</h3></v-list-item-title>
                        <v-list-item-subtitle class="subtitle-content font-white">{{item.description}}</v-list-item-subtitle>
                        <v-list-item-icon class="right-icon" style="margin-bottom:0;">
                          <img src='../../assets/img/arrow.png' width="20" height="6"/>
                        </v-list-item-icon>
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
      lists: []
    }
  },
  mounted() {
    this.getDataList();
  },
  methods:{
      async getDataList(){
        try {
            const { data } = await this.$axios.get('/api/project/list')
            this.setData(data.rows)
        } catch (error) {
            //
        }
      },
      setData(data){
          this.lists = data;
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
  box-shadow: 0 0 20px #ddd !important;
  transform: translateY(-10px);
  transition: transform .8s;
  .font-white{
    // color: #FFF;
  }
}
</style>
