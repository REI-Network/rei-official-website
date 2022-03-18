<template>
  <div>
    <v-container class="align-center">
      <v-row class="mt-10">
        <v-col>
          <v-icon>mdi-tree-outline</v-icon>
          <h2>Community Hub</h2>
          <v-row class="mt-10 font-white" justify="space-between">
            <div class="Hub">
              <div class="hub-background twitter">
                <div class="hub-name">Twitter <v-icon color="#FFF">～</v-icon></div>
                <h2>≈ 94,330</h2>
                <div>Members</div>
              </div>
              <div class="hub-background reddit">
                <div class="hub-name">Reddit <v-icon color="#FFF">～</v-icon></div>
                <h2>≈ 94,330</h2>
                <div>Members</div>
              </div>
            </div>
            <div class="Hub">
              <div class="hub-background github">
                <div class="hub-name">GitHub <v-icon color="#FFF">～</v-icon></div>
                <h2>≈ 94,330</h2>
                <div>Members</div>
              </div>
              <div class="hub-background kakao">
                <div class="hub-name">KaKao <v-icon color="#FFF">～</v-icon></div>
                <h2>≈ 94,330</h2>
                <div>Members</div>
              </div>
            </div>
            <div class="Hub">
              <div class="hub-background discord">
                <div class="hub-name">Discord <v-icon color="#FFF">～</v-icon></div>
                <h2>≈ 94,330</h2>
                <div>Members</div>
              </div>
            </div>
          </v-row>
          <v-row class="mt-10">
            <div class="telegram">

            </div>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      banner: require('@/assets/img/ecosystem/banner.png')
    }
  },
  components: {

  },
}
</script>

<style lang="scss" scoped>
.align-center{
}
.font-white{
  color: #FFF;
}
.Hub{
  width: 32%;
  .hub-background{
    height: 23rem;
    margin-top: 1.2rem;
    width: 96%;
    background-color: lightgreen;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: flex-end;
    padding-right: 2rem;
    padding-bottom: 2rem;
    .hub-name{
      font-size: 28px;
    }
  }
  .hub-background:hover{
    box-shadow:rgb(0 0 0 / 10%) 0px 0px 10px;
  }
  .twitter{
    background: linear-gradient(to bottom, #1B9BE6, #9EDFFF);
  }
  .reddit{
    background: linear-gradient(to bottom, #FF744D, #FFA78A);
  }
  .github{
    background: linear-gradient(to bottom, #7E707E, #B1B3B1);
  }
  .kakao{
    background: linear-gradient(to bottom, #FFCE6B, #FBD99B);
  }
  .discord{
    margin-top: 1.2rem;
    width: 96%;
    height: 47.25rem;
    background: linear-gradient(to bottom, #8A92CE, #B6C5F5);
  }
}
</style>
