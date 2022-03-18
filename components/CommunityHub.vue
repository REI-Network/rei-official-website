<template>
  <div>
    <v-container class="align-center">
      <v-row class="mt-10">
        <v-col>
          <v-row>
            <h2>Community Hub</h2>
          </v-row>
          <v-row class="mt-10 font-white" justify="space-between">
            <div class="Hub">
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="hub-background mt-10 twitter"
                  >
                  <img src="@/assets/img/ecosystem/exchange.png" height="200" width="200" />
                  <div class="hub-content">
                    <div class="hub-name font-white">Twitter <v-icon color="#FFF">～</v-icon></div>
                    <h2 class=" font-white">≈ 94,330</h2>
                    <div class="font-white">Members</div>
                  </div>
                </v-card>
              </v-hover>
               <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="hub-background mt-10 reddit"
                  >
                  <img src="@/assets/img/ecosystem/exchange.png" height="200" width="200" />
                  <div class="hub-content">
                    <div class="hub-name font-white">Redditt <v-icon color="#FFF">～</v-icon></div>
                    <h2 class=" font-white">≈ 94,330</h2>
                    <div class="font-white">Members</div>
                  </div>
                </v-card>
              </v-hover>
            </div>
            <div class="Hub">
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="hub-background mt-10 github"
                  >
                  <img src="@/assets/img/ecosystem/exchange.png" height="200" width="200" />
                  <div class="hub-content">
                    <div class="hub-name font-white">GitHub <v-icon color="#FFF">～</v-icon></div>
                    <h2 class=" font-white">≈ 94,330</h2>
                    <div class="font-white">Members</div>
                  </div>
                </v-card>
              </v-hover>
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="hub-background mt-10 kakao"
                  >
                  <img src="@/assets/img/ecosystem/exchange.png" height="200" width="200" />
                  <div class="hub-content">
                    <div class="hub-name font-white">KaKao <v-icon color="#FFF">～</v-icon></div>
                    <h2 class=" font-white">≈ 94,330</h2>
                    <div class="font-white">Members</div>
                  </div>
                </v-card>
              </v-hover>
            </div>
            <div class="Hub">
            <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="hub-background mt-10 discord"
                  >
                  <img src="@/assets/img/ecosystem/exchange.png" height="200" width="200" />
                  <div class="mt-16 hub-content">
                    <div class="hub-name font-white">Discord <v-icon color="#FFF">～</v-icon></div>
                    <h2 class=" font-white">≈ 94,330</h2>
                    <div class="font-white">Members</div>
                  </div>
                </v-card>
              </v-hover>
            </div>
          </v-row>
          <v-row class="mt-12 telegram font-white" justify="space-between">
            <div class="left-telegram">
                <div class="hub-name">Telegram <v-icon color="#FFF">～</v-icon></div>
                <h2>≈ 94,330</h2>
                <div>Members</div>
            </div>
            <div class="right-telegram">
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>

              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
              <div class="nation">
                <img src="@/assets/img/ecosystem/banner.png" alt="" class="img-head">
                <div>English</div>
                <div>Community</div>
              </div>
            </div>
          </v-row>
          <v-row class="mt-16">
            <div class="learn-join">
              <div><v-img :src="banner4" class="img-style-learn"/></div>
              <div class="bounty">
                <h3 class="font-gradient">$1,500,000 For Bug Bounty!#REI #Mainnet</h3>
                <p class="font-white">If Ypu Find A Bug Or Have Any Ideas Which Will Improve Mainnet Security.Piz Contact Us</p>
              </div>
              <div class="tow-btn">
                <v-btn
                  color="#1D10F8"
                  class="btn-background font-white"
                  width="120"
                  height="36"
                >
                  Learn More
                </v-btn>
                <v-btn
                  color="green"
                  class="btn-background font-white"
                  width="120"
                  height="36"
                >
                  Submit
                </v-btn>
              </div>
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
      banner: require('@/assets/img/ecosystem/banner.png'),
      banner4: require('@/assets/img/ecosystem/REIiconDeveloperCommunity.png')
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
    width: 96%;
    height: 23rem;
    background-color: lightgreen;
    padding-right: 2rem;
    .hub-content{
      margin-top:2rem;text-align:right;
    }
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
    width: 100%;
    height: 48.5rem;
    background: linear-gradient(to bottom, #8A92CE, #B6C5F5);
    .hub-content{
      margin-top: 2orem;
    }
  }
}
.hub-name{
  font-size: 28px;
}
.telegram{
  // width: 100%;
  height: 23rem;
  font-size: 14px;
  background: linear-gradient(to bottom, #78B8DE, #B4E7FF);
  .left-telegram{
    width: 31%;
    height: 23rem;
    // background: red;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: flex-end;
    padding-right: 2rem;
    padding-bottom: 2rem;
  }
  .right-telegram{
    width: 62%;
    height: 72%;
    margin-top: 5%;
    margin-right: 4%;
    // background: blue;
    display: flex;
    justify-content: space-around;
    flex-flow: wrap;
    align-items: center;
    .nation{
      width: 13%;
      // background: green;
      text-align: center;
    }
    .img-head{
      height: 4rem;
      width: 4rem;
      border-radius: 2.5rem;
    }
  }
}

.learn-join{
  height: 8rem;
  width: 100%;
  background-color: pink;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background: linear-gradient(to bottom right, #3E1D8C, #715FA3);
  .img-style{
    width: 6rem;
    height: 8rem;
  }
  .img-style-learn{
    width: 4.6rem;
    height: 6.8rem;
  }
  .tow-btn{
    display: flex;
    flex-direction: column;
  }
  .btn-background{
    background-color: blue;
    border-radius: 30px;
    cursor: pointer;
    font-weight: 700;
    margin: 4px 0;
  }
  .font-gradient{
    background: linear-gradient(to right, #FFF0B5, #FFADBF);
    -webkit-background-clip: text;
    color: transparent;
  }
}
</style>
