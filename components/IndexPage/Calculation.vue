<template>
  <div>
    <v-container class="stake-container">
      <v-row justify="space-between" class="stake">
        <v-col class="stake-left">
          <div class="stake-text">Vote on REI Network</div>
          <div class="font-grey earn-rewards">
            Earn rewards by voting your $REI to help secure the REI network.
            <br />Choose nodes and start earning in just a few clicks.
          </div>
          <v-btn class="stake-btn">
            <a href="https://dao.rei.network/#/stake" target="_blank"
              >Vote Now
            </a></v-btn
          >
          <ul class="font-grey">
            <li>Up to 10% APR for a one-year commitment to voting</li>
            <li>Share the rewards with nodes</li>
            <li>
              Note: This calculation of earnings is for reference only and does
              not represent the final earnings, please refer to the actual
              results
            </li>
          </ul>
        </v-col>
        <v-col class="stake-right">
          <div class="font-grey">
            Please select an activated node to estimate rewards
          </div>
          <v-select
            class="elevation-0 select-rate"
            v-model="value"
            :items="calculationItems"
            style=""
            background-color="#FFF"
            dense
            outlined
            :append-icon="mdiMenuDown"
            return-object
            :menu-props="{ bottom: true, offsetY: true }"
          >
            <template slot="selection" slot-scope="data">
              <v-row justify="space-between">
                <v-col cols="12" md="6" class="nodeName"
                  ><span>{{ data.item.nodeName }}</span
                  >&nbsp;&nbsp;&nbsp;{{ data.item.address | addr }}</v-col
                >
                <v-col class="font-grey commission"
                  >Commission Rate:{{ data.item.commissionRate }}%</v-col
                >
              </v-row>
            </template>
            <template #item="{ item }">
              <v-row
                justify="space-between"
                style="background-color: transparent"
              >
                <v-col cols="12" md="6" class="nodeName"
                  ><span v-if="item.nodeName != ''">{{ item.nodeName }}</span
                  >&nbsp;&nbsp;&nbsp;{{ item.address | addr }}</v-col
                >
                <v-col class="font-grey commission"
                  >Commission Rate:{{ item.commissionRate }}%</v-col
                >
              </v-row>
            </template>
          </v-select>
          <v-row class="calculate-input">
            <span class="subheading mr-1 font-grey">Vote</span>
            <!-- <span
                class="text-h6 font-weight-light font-amount"
              >{{stake | asset(2)}}</span> -->
            <div style="width: 200px">
              <v-text-field
                class="font-blue"
                style="font-size: 24px"
                v-model="stake"
                color="#2116E5"
              ></v-text-field>
            </div>
            <span class="subheading font-weight-light mr-1 font-grey">REI</span>
          </v-row>
          <!-- <v-slider
            v-model="stake"
            track-color="white"
            track-fill-color="#2116E5"
            thumb-color="#2116E5"
            tick-size="10"
            loader-height="10"
            always-dirty
            min="0"
            max="2000000"
          >
          </v-slider>
          <v-row justify="space-between" class="slider-num font-grey">
            <v-col>0</v-col>
            <v-col style="text-align: right">2M</v-col>
          </v-row> -->
          <v-row class="" justify="space-between">
            <v-col class="text-left">
              <span
                class="font-weight-light mr-1 font-grey"
                style="margin-left: 8px"
                >Locking $REI for</span
              >
              <span class="font-blue font-amount" v-text="days"></span>
              <span class="font-weight-light mr-1 font-grey"> days</span>
            </v-col>
          </v-row>
          <v-slider
            v-model="days"
            track-color="#F1F5F8"
            track-fill-color="#2116E5"
            thumb-color="#2116E5"
            always-dirty
            min="0"
            max="365"
            tick-size="8"
          >
          </v-slider>
          <v-row justify="space-between" class="slider-num font-grey">
            <v-col>0 D</v-col>
            <v-col style="text-align: right">365D</v-col>
          </v-row>
          <v-row justify="space-between" style="padding: 0 8px">
            <v-col class="font-grey">
              <div>Estimated rewards</div>
              <div>
                <span class="font-blue">{{ userRewardsYear | asset(2) }}</span>
                REI
              </div>
            </v-col>
            <v-col class="font-grey" style="text-align: right">
              <div>Current APR</div>
              <div>
                <span class="font-blue">{{ current | asset(2) }}</span> %
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
import { mdiMinus, mdiPlus, mdiMenuDown } from "@mdi/js";
import filters from "../../filters";
import find from "lodash/find";

export default {
  name: "IndexPage",
  filters,
  data() {
    return {
      stake: 0,
      days: 0,
      interval: null,
      isPlaying: false,
      mdiMinus,
      mdiPlus,
      mdiMenuDown,
      value: "",
      userRewardsYear: 0,
      current: 0,
      totalAmount: 0,
      detailsList: [],
      calculationItems: [
        {
          isActive: "true",
          address: "0x0efe0da2b918412f1009337FE86321d88De091fb",
          power: "842260.451381566421091339",
          commissionRate: "20",
          updateTimestamp: "0",
        },
        {
          isActive: "true",
          address: "0xb7a19F9b6269C26C5Ef901Bd128c364Dd9dDc53a",
          power: "801642.123077179946052706",
          commissionRate: "40",
          updateTimestamp: "0",
        },
        {
          isActive: "true",
          address: "0x2957879B3831b5AC1Ef0EA1fB08Dd21920f439b4",
          power: "801197.998498132164915841",
          commissionRate: "60",
          updateTimestamp: "0",
        },
        {
          isActive: "true",
          address: "0x1b0885d33B43A696CD5517244A4Fcb20B929F79D",
          power: "800943.963042040083177791",
          commissionRate: "80",
          updateTimestamp: "0",
        },
        {
          isActive: "true",
          address: "0xaA714ecc110735B4E114C8B35F035fc8706fF930",
          power: "801005.796556894099742228",
          commissionRate: "100",
          updateTimestamp: "0",
        },
      ],
    };
  },
  components: {},
  watch: {
    listenChange(stake, days) {
      this.Calculation();
    },
    value: function (newVal, oldVal) {
      this.Calculation();
      this.getValidatorDetails();
    },
  },
  computed: {
    listenChange() {
      const { stake, days } = this;
      return {
        stake,
        days,
      };
    },
  },
  mounted() {
    this.getValidatorDetails();
    this.getCalculation();
  },
  methods: {
    toggle() {
      this.isPlaying = !this.isPlaying;
    },
    async getValidatorDetails() {
      const { data } = await this.$axios.get(
        "https://dao.rei.network/data/validator/validator-list.json"
      );
      this.detailsList = data.data;
    },
    async getCalculation() {
      const { data } = await this.$axios.get(
        "https://gateway.rei.network/api/validator"
      );
      this.totalAmount = data.data.totalAmount;
      let activeList = data.data.activeList;
      this.calculationItems = activeList.map((item) => {
        let detail = find(
          this.detailsList,
          (items) =>
            items.nodeAddress.toUpperCase() == item.address.toUpperCase()
        );
        var nodeName = "";
        if (detail) {
          nodeName = detail.nodeName;
        } else {
          nodeName = "";
        }
        return {
          ...item,
          nodeName: nodeName,
        };
      });
      function sortArr(attr) {
        return function (a, b) {
          return b[attr] - a[attr];
        };
      }
      this.calculationItems = this.calculationItems.sort(
        sortArr("commissionRate")
      );
      this.value = this.calculationItems[0];
    },
    Calculation() {
      let votingRewardsYear =
        10000000 *
        ((parseFloat(this.value.power) + this.stake) /
          (this.totalAmount + this.stake)) *
        (this.value.commissionRate / 100);
      let UserRewards =
        ((votingRewardsYear * this.stake) /
          (parseFloat(this.value.power) + this.stake) /
          365) *
        this.days;
      this.userRewardsYear = UserRewards;
      if (this.userRewardsYear === 0) {
        this.current = 0;
      } else {
        this.current = (UserRewards / (this.stake * 365)) * this.days * 100;
      }
    },
  },
};
</script>

<style scoped lang="scss">
.stake-container {
  // height:760px;
  max-width: 1220px;
  .stake {
    border-radius: 4px;
    background-color: #f2f5f8;
    margin: 12px 0px 0px 0px;
    padding: 60px 40px;
  }
  .stake-left {
    .earn-rewards {
      margin-top: 16px;
    }
    .stake-btn {
      background-color: blue;
      color: #fff;
      border-radius: 20px;
      margin: 28px 0;
    }
    ul {
      li {
        margin: 14px 0;
      }
    }
  }
  .font-grey {
    // font-size: 14px;
    color: #7e7e7e;
  }
  .stake-text {
    font-size: 32px;
    font-weight: bolder;
  }
  .stake-right {
    border-radius: 8px;
    background-color: #fff;
    padding: 20px;
  }
  .font-amount {
    color: #2116e5;
  }
  .slider-num {
    padding: 0 12px;
    margin-top: -40px;
  }
  .select-rate {
    border-radius: 20px;
    margin: 12px 0;
  }
  .font-blue {
    // font-family: babes !important;
    color: #2116e5;
    font-size: 24px;
    font-weight: bolder;
  }
}
.subheading {
  height: 30px;
  margin-top: 20px;
  margin-left: 20px;
}
a {
  color: #fff;
  text-decoration: none;
}
.nodeName {
  font-size: 14px;
  font-weight: bold;
}
.commission {
  font-size: 14px;
}
.calculate-input {
  margin-top: -20px;
}
@keyframes metronome-example {
  from {
    transform: scale(0.5);
  }

  to {
    transform: scale(1);
  }
}
</style>
