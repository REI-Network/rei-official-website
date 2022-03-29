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
                  :src="item.img">
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
          <h2>News</h2>
          <v-row>
            <v-col cols="4" md="4" v-for="(item,i) in news">
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
      news:['<blockquote class="twitter-tweet"><p lang="en" dir="ltr">We&#39;re happy to announce that <a href="https://twitter.com/search?q=%24REI&amp;src=ctag&amp;ref_src=twsrc%5Etfw">$REI</a> is listed on <a href="https://twitter.com/imTokenOfficial?ref_src=twsrc%5Etfw">@imTokenOfficial</a>- an easy and secure digital wallet!ðŸ›¡ï¸<br><br>Comment to let us know which wallet you most want to support <a href="https://twitter.com/search?q=%24REI&amp;src=ctag&amp;ref_src=twsrc%5Etfw">$REI</a> Token. We will reach out to the team for the listingðŸ›©<a href="https://twitter.com/hashtag/imtoken?src=hash&amp;ref_src=twsrc%5Etfw">#imtoken</a> <a href="https://twitter.com/hashtag/GXChain?src=hash&amp;ref_src=twsrc%5Etfw">#GXChain</a> <a href="https://twitter.com/hashtag/EVM?src=hash&amp;ref_src=twsrc%5Etfw">#EVM</a> <a href="https://twitter.com/hashtag/Crypto?src=hash&amp;ref_src=twsrc%5Etfw">#Crypto</a> <a href="https://twitter.com/hashtag/REINetwork?src=hash&amp;ref_src=twsrc%5Etfw">#REINetwork</a> <a href="https://twitter.com/hashtag/Blockchain?src=hash&amp;ref_src=twsrc%5Etfw">#Blockchain</a> <a href="https://t.co/G4MidkGaug">pic.twitter.com/G4MidkGaug</a></p>&mdash; REI Networkï½œFrom #GXChain! (@GXChainGlobal) <a href="https://twitter.com/GXChainGlobal/status/1501457225444777990?ref_src=twsrc%5Etfw">March 9, 2022</a></blockquote>',
'<blockquote class="twitter-tweet"><p lang="en" dir="ltr"><a href="https://twitter.com/hashtag/REINetwork?src=hash&amp;ref_src=twsrc%5Etfw">#REINetwork</a> is delighted to announce the partnership with <a href="https://twitter.com/SupraOracles?ref_src=twsrc%5Etfw">@SupraOracles</a> ðŸ”¥<br><br>SupraOracles strives to bridge the gap between traditional capital markets and the <a href="https://twitter.com/hashtag/Web3?src=hash&amp;ref_src=twsrc%5Etfw">#Web3</a> ecosystem.<br><br>Letâ€™s get superb with Supra!ðŸ¦¸<a href="https://twitter.com/hashtag/oracle?src=hash&amp;ref_src=twsrc%5Etfw">#oracle</a> <a href="https://twitter.com/hashtag/GXChain?src=hash&amp;ref_src=twsrc%5Etfw">#GXChain</a> <a href="https://twitter.com/hashtag/EVM?src=hash&amp;ref_src=twsrc%5Etfw">#EVM</a> <a href="https://twitter.com/hashtag/Crypto?src=hash&amp;ref_src=twsrc%5Etfw">#Crypto</a> <br>More details: <a href="https://t.co/7IrDf2rtLz">https://t.co/7IrDf2rtLz</a></p>&mdash; REI Networkï½œFrom #GXChain! (@GXChainGlobal) <a href="https://twitter.com/GXChainGlobal/status/1501393418102067206?ref_src=twsrc%5Etfw">March 9, 2022</a></blockquote>',
'<blockquote class="twitter-tweet"><p lang="en" dir="ltr">ðŸŽ‰ <a href="https://twitter.com/hashtag/REINetwork?src=hash&amp;ref_src=twsrc%5Etfw">#REINetwork</a> Content Bounty Program is up and running! ðŸŽ‰<br><br>ðŸ’° Create content to talk about <a href="https://twitter.com/hashtag/REINetwork?src=hash&amp;ref_src=twsrc%5Etfw">#REINetwork</a>, let&#39;s spread the word out and get rewarded with juicy <a href="https://twitter.com/search?q=%24REI&amp;src=ctag&amp;ref_src=twsrc%5Etfw">$REI</a> rewards! ðŸ’°<br><br>Send your submission here: <a href="https://t.co/SjIHrTO8j2">https://t.co/SjIHrTO8j2</a><a href="https://twitter.com/hashtag/GXChain?src=hash&amp;ref_src=twsrc%5Etfw">#GXChain</a> <a href="https://twitter.com/hashtag/bounty?src=hash&amp;ref_src=twsrc%5Etfw">#bounty</a> <a href="https://twitter.com/hashtag/Crypto?src=hash&amp;ref_src=twsrc%5Etfw">#Crypto</a><a href="https://t.co/YfCldTl2SG">https://t.co/YfCldTl2SG</a></p>&mdash; REI Networkï½œFrom #GXChain! (@GXChainGlobal) <a href="https://twitter.com/GXChainGlobal/status/1500774283223580673?ref_src=twsrc%5Etfw">March 7, 2022</a></blockquote>']
    }
  },
  mounted() {
    this.getDataList();
  },
  methods:{
      async getDataList(){
        try {
            const { data } = await this.$axios.get('/api/news/list')
            console.log(data)
            this.setData(data.rows)
        } catch (error) {
            //
        }
      },
      setData(data){
          let _data = [].concat(data);
          this.lists = _data.slice(0,4);
          this.otherLists = _data.slice(4);
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

