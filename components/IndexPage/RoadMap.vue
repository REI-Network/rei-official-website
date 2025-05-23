<template>
  <div style="width:100%">
    <v-container class="mt-12 content-width">
        <h1 style="margin-bottom:72px">Roadmap <span style="font-size: 20px;"><img width="80" src="../../assets/img/new_release.png"></span></h1>
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
            <li v-if="item.content1" v-html="item.content1"></li>
            <li v-if="item.content2" v-html="item.content2"></li>
            <li v-if="item.content3" v-html="item.content3"></li>
            <li v-if="item.content4" v-html="item.content4"></li>
            <li v-if="item.content5" v-html="item.content5"></li>
            <li v-if="item.content6" v-html="item.content6"></li>
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
                time: "2025 Q2",
                text: "",
                content1:"<strong>Core Performance:</strong> Monitor node activity to optimize block‐producing network; phase out high‐miss, long‐offline nodes",
                content2:"<strong>AI Integration:</strong> Publish AI module API spec; launch REI MCP framework and AI Agent developer program",
                content3:"<strong>Cross-Chain:</strong> Onboard a third-party Bridge for BSC assets",
                content4:"<strong>Stake-to-Earn:</strong> Combine token rewards with partner airdrops (USDT/BUSD/partner tokens) to boost staking; partner DApps and bridges run multiple airdrop rounds for active stakers",
                content5:"<strong>Gas-Free UX:</strong> Introduce stablecoins to enable gas-free payments, voting, gaming, etc.",
            },
            {
                time: "2025 Q3",
                text: "",
                content1:"<strong>Core Performance:</strong> Upgrade P2P layer to reduce sync latency ",
                content2:"<strong>AI Integration:</strong> Deepen native AI module support ",
                content3:"<strong>Gas-Free UX:</strong> Expand gas-free use cases alongside stablecoin rollout",
            },
            {
                time: "2025 Q4",
                text: "",
                content1:"<strong>Core Performance:</strong> “Block Acceleration” testnet: shorten block time from 3s to 1.5s ",
                content2:"<strong>AI Integration:</strong> Launch REI MCP Marketplace; provide gas subsidies for top AI Agents ",
                content3:"<strong>Cross-Chain:</strong> Add Solana-compatible bridge for broader interoperability ",
                content4:"<strong>Stake-to-Earn:</strong> Roll out gas-free airdrop subsidies; “stake‐to‐mine + airdrop” model with DEX fee credits and gas refunds ",
                content5:"<strong>Gas-Free UX:</strong> Host “Gas-Free Swap” events for major asset pairs to boost liquidity ",
            },
            {
                time: "2026 Q1",
                text: "",
                content1:"<strong>Performance Optimization:</strong> Continue testnet validation of 1.5s block times.",
                content2:"<strong>Cross-Chain Infrastructure:</strong> Further optimize Solana cross-chain compatibility.",
                content3:"<strong>Stake-to-Earn Incentives: </strong>Implement targeted, multi-metric incentives—based on on-chain activity, DApp usage, and holding duration—to maximize resource efficiency and drive genuine growth.",
            },
            {
                time: "2026 Q2",
                text: "",
                content1:"<strong>Performance Optimization:</strong> Deploy 1.5s block production on mainnet based on test feedback, supporting high-frequency interactions.",
                content2:"<strong>Cross-Chain Infrastructure:</strong> List cross-chain assets on REI Network’s DEX and attract mainstream liquidity through incentive programs.",
            },
            {
                time: "By 2026 Q3",
                text: "",
                content1:"<strong>Gasless Use Cases:</strong> Partner with Web3 applications to roll out gas-free payment scenarios, exploring on-chain payments and daily consumer use cases.",
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
