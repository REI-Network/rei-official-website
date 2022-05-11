<template>
  <div style="width:100%">
    <v-container class="mt-12 content-width">
        <h1 style="margin-bottom:72px">Roadmap</h1>
            <v-timeline
             v-for="(item, i) in items"
            :key="i"
            dense
            align-top
            >

    <v-timeline-item color="#2340f0" small class="text-left timeline">
       <div class="time-content">
         <span class="pa-5 font-weight-bold">{{item.time}}</span>
          <div class="pa-5 time-text">{{item.text}}</div>
          <ul class="road-content">
            <li v-if="item.content1">{{item.content1}}</li>
            <li v-if="item.content2">{{item.content2}}</li>
            <li v-if="item.content3">{{item.content3}}</li>
            <li v-if="item.content4">{{item.content4}}</li>
            <li v-if="item.content5">{{item.content5}}</li>
            <li v-if="item.content6">{{item.content6}}</li>
          </ul>
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
                time: "2021.Q2",
                text: "",
                content1:"GXChain 2.0 developer Preview Version released, and the code is officially open-sourced",
                content2:"GXChain 2.0 testnet released, supports EVM and Ethereum general infrastructure, and is based on POA consensus; GXChain 2.0 testnet block explorer launched",
            },
            {
                time: "2021.Q3",
                text: "",
                content1:"GXChain 2.0 testnet was upgraded, and stacking and slashing modules were introduced to realize second-level block confirmation",
            },
            {
                time: "2021.Q4",
                text: "",
                content1:"GXChain 2.0 testnet was upgraded to realize the free economic model",
                content2:"GXChain 2.0 was officially renamed REI network. GXChain 1.0 and REI network are interconnected & CrossChain through GXC-Relay",
            },
            {
                time: "Eureka  2022.Q1",
                text: "The singularity of the rebrand from GXChain to REI Network.",
                content1:"Compatible with EVM and Ethereum infrastructure, fast transaction confirmation through DPoS+BFT",
                content2:"FreeStake (Free Economic Model) testnet was live",
                content3:"$GXC-$REI token swap",
                content4:"REI Network ecosystem infrastructure construction, ecosystem blueprint and brand building plan",
            },
            {
                time: "Tribes  2022.Q2",
                text: "The tribe is the source of human civilization. At this stage, the development of REI Network will be accelerated.",
                content1:"REI Network connects with mainstream blockchain ecosystems",
                content2:"REI Network project and ecosystem growth plan released (Users, TVL)",
                content3:"FreeStake (Free Economic Model) mainnet is launched",
                content4:"REI DAO Decentralized Governance is live",
                content5:"REI Network Super Node Campaign is started",
                content6:"REI Network Brand Building: covers the world’s major crypto markets",
            },
            {
                time: "Federation  2022.Q3-Q4",
                text: "The Federation is a more modern and efficient paradigm for human society and civilization. At this stage, REI Network will focus on building a more organized, scaled, and oriented ecosystem:",
                content1:"Reconstruct RPC, P2P network, consensus mechanism, and virtual machine module to achieve 2–3 times overall performance improvement",
                content2:"Explore modular public chain technology, and the integration of Rollups, sharding, multi-chain, and other technologies with REI Network ",
                content3:"Large-scale projects and ecosystem growth cycle on REI Network (Users, TVL) ",
                content4:"Field focused growth: accelerate field growth plans for Free Economic Model (DeFi, GameFi, NFT, SocialFi, etc.) ",
                content5:"Strengthen brand recognition of REI Network: expanding the global space",
                content6:"",
            },
            {
                time: "Spreading  2023",
                text: "REI Network will commit itself to improve performance and applying native assets to more areas, expanding global acceptance:",
                content1:"Solve the Trilemma of public chain through modular public chain technology, achieve a hundredfold performance improvement of REI Network under the premise of security and decentralization",
                content2:"REI Network is further accepted by global users",
                content3:"$REI, the native asset: covers more fields and use cases",
                content4:"The public welfare attribute of REI Network: playing an inclusive social role",
                content5:"",
                content6:"",
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
  // padding-top:20px;
  padding-bottom:20px;
}
    .time-content:hover{
      padding-top:12px;
      padding-bottom:8px;
      background-color: #F2F5F8;
      transform: translateY(-10px);
      transition: transform .8s;
      .time-text{
        font-weight: bold;
      }
    }
  .road-content{
    color: #828293;
    margin-left: 12px;
    font-size: 15px;
    li{
      padding: 5px 0;
    }
  }
</style>
