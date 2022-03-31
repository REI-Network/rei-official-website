<template>
  <div style="width:100%">
    <v-container class="mt-12 content-width">
        <h1 style="margin-bottom:72px">Roadmap</h1>
            <v-timeline
             v-for="(item, i) in items"
            :key="i"
            dense
            >

    <v-timeline-item color="#2340f0" small class="text-left timeline">
       <div class="time-content">
         <span class="pa-5 font-weight-bold">{{item.time}}</span>
      <div class="pa-5">{{item.text}}</div>
       </div>
    </v-timeline-item>
  </v-timeline>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
      return {
        reverse: true,
        items:[
            {
                time: "2021.04",
                text: "GXChain 2.0 developer Preview Version released, and the code is officially open-sourced"
            },
            {
                time: "2021.06",
                text: "GXChain 2.0 testnet released, supports EVM and Ethereum general infrastructure, and is based on POA consensus; GXChain 2.0 testnet block explorer launched"
            },
            {
                time: "2021.08",
                text: "GXChain 2.0 testnet was upgraded, and stacking and slashing modules were introduced to realize second-level block confirmation"
            },
            {
                time: "2021.10",
                text: "GXChain 2.0 testnet was upgraded to realize the free economic model"
            },
            {
                time: "2021.12",
                text: "GXChain 2.0 was officially renamed REI network. GXChain 1.0 and REI network are interconnected & CrossChain through GXC-Relay"
            },
            {
                time: "2022",
                text: "REI Network ecological construction; Function optimization and infrastructure upgrading of governance module and stacking module"
            },
        ]
      }
  },
  components: {

  },
}
</script>
<style scoped lang="scss">
.content-width{
    max-width: 1220px;
  }
.time-content{
  padding-top:20px;
  padding-bottom:12px;
}
    .time-content:hover{
      font-weight: bold;
       background-color: #F2F5F8;
      transform: translateY(-10px);
      transition: transform .8s;
    }
</style>
