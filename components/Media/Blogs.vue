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
                  v-for="(item,i) in lists"
                  :key="i"
                  :src="item.img"
                >
                  </v-carousel-item>
                </v-carousel>
                <v-list three-line style="padding:0;">
                    <v-list-item class="list-content">
                      <v-list-item-content>
                        <v-list-item-title>{{lists.length>0?lists[model].title:''}}</v-list-item-title>
                        <v-list-item-subtitle class="subtitle-content">{{lists.length>0?lists[model].desc:0}}</v-list-item-subtitle>
                      </v-list-item-content>
                      <v-list-item-action>
                        <v-btn
                          color="#1D10F8"
                          class="font-white"
                          width="120"
                          height="36"
                          :href="lists.length>0?lists[model].link:''"
                          target="_blank"
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
              <v-card class="right-content"  
                  v-for="(item,i) in otherLists"
                  :key="i"
                  :src="item.img"
                  @click="goto(item.link)"
                  >
                  
                <v-img :src="item.img" width="100%"  :aspect-ratio="16/9" />
                <v-list two-line>
                  <v-list-item>
                    <v-list-item-content>
                        <v-list-item-title>{{item.title}}</v-list-item-title>
                        <v-list-item-subtitle class="subtitle-content">{{item.desc}}</v-list-item-subtitle>
                      </v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-card>
              
            </v-col>
          </v-row>
          <h2 class="my-12">News</h2>
          <v-row>
            <v-col cols="4" md="4" v-for="(item,i) in news" :key="i">
                <div v-html="item"></div>
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
      lists: [],
      otherLists:[],
      news:[]
    }
  },
  mounted() {
    this.getDataList();
    this.getLatestNews();
  },
  methods:{
      async getDataList(){
        try {
            const { data } = await this.$axios.get('/api/news/list')
            console.log(data)
            this.setData(data.rows)
        } catch (error) {
            console.log(error)
        }
      },
      async getLatestNews(){
          try {
            const { data } = await this.$axios.get('/api/twitter/list')
            if(data.rows.length>0){
                let list = data.rows
                this.news = list.map((item) =>{
                    return item.json.replace(/<script.*<\/script>/gm, "")
                });
            }
        } catch (error) {
            console.log(error)
        }
      },
      setData(data){
          let _data = [].concat(data);
          this.lists = _data.slice(0,4);
          this.otherLists = _data.slice(4);
      },
      goto(href) {
        window.open(href)
      },
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

