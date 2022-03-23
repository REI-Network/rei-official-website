<template>
  <div>
    <v-container class="mt-12">
        <h2>Roadmap</h2>
        <v-row no-gutters 
            v-for="(item, i) in items"
            :key="i">
            <v-col
                cols="12"
                md="2"
            >
                <div class="pa-5">
                    {{item.time}}
                </div>
            </v-col>
            <v-col
                cols="12"
                md="10"
            >
                <div class="pa-5">
                    {{item.text}}
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
