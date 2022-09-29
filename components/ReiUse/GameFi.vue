<template>
  <div>
    <v-container class="mt-12 align-item">
      <h1>Projects</h1>
      <!-- <v-tabs hide-slider>
        <v-chip-group active-class="chip_group" v-model="intervalModel" mandatory>
        <v-tab>
          <v-chip class="ma-2"> All </v-chip>
        </v-tab>
        <v-tab>
          <v-chip class="ma-2"> NFT </v-chip>
        </v-tab>
        <v-tab>
          <v-chip class="ma-2"> GameFi </v-chip>
        </v-tab>
        <v-tab>
          <v-chip class="ma-2"> DeFi </v-chip>
        </v-tab>
        </v-chip-group>
      </v-tabs> -->
      <v-row align="center">
        <v-chip-group
          active-class="chip_group"
          v-model="intervalModel"
          mandatory
        >
          <v-chip class="ma-2" x-small v-for="tag in tags" :key="tag.query" @click="getList(tag)">
            {{ tag.title }}
          </v-chip>
        </v-chip-group>
      </v-row>
      <v-row class="mt-8">
        <v-col
          cols="12"
          sm="4"
          class="project-background"
          v-for="(item, i) in lists"
          :key="i"
        >
          <!-- v-for="(item,i) in Lists"
              :key="i" -->
          <v-hover v-slot="{ hover }" open-delay="200">
            <v-card
              elevation="0"
              :class="{ 'on-hover': hover }"
              @click="goto(item.app_url)"
            >
              <v-list two-line class="list-item">
                <v-list-item>
                  <v-list-item-avatar size="80">
                    <v-img :src="item.logo"></v-img>
                  </v-list-item-avatar>
                  <v-list-item-content>
                    <v-list-item-title class="font-white"
                      ><h3>{{ item.app_name }}</h3></v-list-item-title
                    >
                    <v-list-item-subtitle class="subtitle-content font-white">{{
                      item.description
                    }}</v-list-item-subtitle>
                    <v-list-item-icon
                      class="right-icon"
                      style="margin-bottom: 0"
                    >
                      <img
                        src="../../assets/img/arrow.png"
                        width="20"
                        height="6"
                      />
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
      intervalModel: 0,
      lists: [],
      // tags: ["All", "NFT", "GameFi", "DeFi"],
      tags: [
        {
          query:"",
          title:"All",
        },
        {
          query:"NFT",
          title:"NFT",
        },
        {
          query:"GameFi",
          title:"GameFi",
        },
        {
          query:"DeFi",
          title:"DeFi",
        }
      ]
    };
  },
  mounted() {
    this.getDataList();
  },
  methods: {
    async getDataList() {
      try {
        const { data } = await this.$axios.get("/api/project/list");
        this.setData(data.rows);
      } catch (error) {
        //
      }
    },
    async getList(value){
      try {
        const { data } = await this.$axios.get(`/api/project/list?type=${value.query}`);
        this.setData(data.rows);
      } catch (error) {
        //
      }
    },
    setData(data) {
      this.lists = data;
    },
    goto(href) {
      window.open(href);
    },
  },
  components: {},
};
</script>

<style lang="scss" scoped>
.align-item {
  max-width: 1220px;
}
.subtitle-content {
  margin-top: 12px;
}
.right-icon {
  display: flex;
  justify-content: flex-end;
  padding-right: 30px;
}
.list-item {
  background-color: #eef3f7;
}
.list-item:hover {
  box-shadow: 0 0 20px #ddd !important;
  transform: translateY(-10px);
  transition: transform 0.8s;
  .font-white {
    // color: #FFF;
  }
}
h1{
  margin-bottom: 20px;
}
.v-chip:not(.v-chip--active) {
  padding: 14px 40px;
  background-color: #f1f5f8;
  border-radius: 20px;
  text-transform: none !important;
}
.v-chip.v-chip--active {
  padding: 14px 40px;
  background-color: red;
  border-radius: 20px;
  text-transform: none !important;
}
.v-application .chip_group {
  background-color: #1d10f8 !important;
  color: #fff;
}
</style>
