<template>
  <div>
    <v-container class="mt-12 align-item" style="overflow: auto;">
        <h1>Compared With Other Blockchains</h1>
        <div class="mt-12 ov-a">
          <table class="compare-table e-table-1">
            <thead>
              <tr>
                <td></td>
                <td>REI Network</td>
                <td>ETH</td>
                <td>Layer2(Rollups)</td>
                <td>Polkadot</td>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(row, i) in list" :key="i">
                <td v-for="(txt, j) in row" :key="j">{{ txt }}</td>
              </tr>
            </tbody>
          </table>
        </div>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      list: [
        ["TPS", "3000+", "10+", "3000+", "1500"],
        ["Finality", "3s", "60 mins", "10 mins", "60s"],
        ["Consensus", "DPoS+BFT", "PoW", "N/A", "NPoS"],
        [
          "Number of validators",
          "21",
          "2 mining pools(51% hash rate)",
          "1",
          "1000",
        ],
        ["Average Transaction Fee", "Free/Cheap", "$40", "Cheap", "Cheap"],
        ["ETH Compatible", "Yes", "-", "Conditional", "Conditional"],
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
.compare-table{
  width: 100%;
  font-size: 14px;
}
.e-table-1 {
  width: 100%;
  border-spacing: 0;
  td {
    padding: 8px 15px;
  }
  thead {
    background-color: #f6f7f8;
    font-weight: bold;
    border-top-left-radius:6px;
  }
  tbody{
    background: #EEF3F7;
  }
  thead tr td{
    padding: 20px;
  }
  tbody tr td:nth-child(1) {
    text-align: right;
    padding-right: 30px;
  }
  tbody tr td:nth-child(2) {
    background-color: #292D3C !important;
    color: #FFF;
    padding: 20px;
    font-weight: bold;
  }
  thead tr td:nth-child(2) {
    background-color: #292D3C;
    color: #FFF;
    font-weight: bold;
  }
  tbody tr:nth-child(even) td {
    background: #f6f7f8;
  }
}
</style>
