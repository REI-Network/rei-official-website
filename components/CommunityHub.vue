<template>
  <div>
    <v-container class="mt-12">
          <h2>Community Hub</h2>
          <v-row class="font-white mt-4" justify="space-between">
            <v-col cols="12" sm="4">
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                   <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="hub-background mt-10 twitter"
                  >
                  <img src="@/assets/img/ecosystem/exchange.png" height="180" width="180" />
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
                  <img src="@/assets/img/ecosystem/exchange.png" height="180" width="180" />
                  <div class="hub-content">
                    <div class="hub-name font-white">Redditt <v-icon color="#FFF">～</v-icon></div>
                    <h2 class=" font-white">≈ 94,330</h2>
                    <div class="font-white">Members</div>
                  </div>
                </v-card>
              </v-hover>
            </v-col>
            <v-col cols="12" sm="4" class="Hub">
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="hub-background mt-10 github"
                  >
                  <img src="@/assets/img/ecosystem/exchange.png" height="180" width="180" />
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
                  <img src="@/assets/img/ecosystem/exchange.png" height="180" width="180" />
                  <div class="hub-content">
                    <div class="hub-name font-white">KaKao <v-icon color="#FFF">～</v-icon></div>
                    <h2 class=" font-white">≈ 94,330</h2>
                    <div class="font-white">Members</div>
                  </div>
                </v-card>
              </v-hover>
            </v-col>
            <v-col cols="12" sm="4">
              <v-hover
                v-slot="{ hover }"
                open-delay="200">
                <v-card
                  tile
                  :elevation="hover ? 12 : 0"
                  :class="{ 'on-hover': hover }"
                  class="hub-background mt-10 discord"
                  >
                  <img src="@/assets/img/ecosystem/exchange.png" height="180" width="180" />
                  <div class="mt-16 hub-content">
                    <div class="hub-name font-white">Discord <v-icon color="#FFF">～</v-icon></div>
                    <h2 class=" font-white">≈ 94,330</h2>
                    <div class="font-white">Members</div>
                  </div>
                </v-card>
                </v-hover>
            </v-col>
          </v-row>
        <v-col>
          <v-row class="mt-10 telegram font-white" justify="space-between">
            <v-col cols="12" sm="6" md="4">
               <div class="left-telegram">
                  <img src="@/assets/img/ecosystem/exchange.png" height="180" width="180" />
                  <div class="mt-10 hub-content">
                    <div class="hub-name font-white">Telegram <v-icon color="#FFF">～</v-icon></div>
                    <h2 class=" font-white">≈ 94,330</h2>
                    <div class="font-white">Members</div>
                  </div>
                </div>
            </v-col >
            <v-col cols="12"  md="8">
              <v-row class="right-telegram" justify="space-around" no-gutters>
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
              </v-row>
              <v-row class="right-telegram" justify="space-around" no-gutters>
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
              </v-row>
            </v-col>
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
  .hub-background{
    height: 22rem;
    background-color: lightgreen;
    padding-right: 2rem;
    .hub-content{
      margin-top:2rem;
      text-align:right;
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
    height: 46.5rem;
    background: linear-gradient(to bottom, #8A92CE, #B6C5F5);
    .hub-content{
      margin-top: 2rem;
    }
  }
.hub-name{
  font-size: 28px;
}
.telegram{
  font-size: 14px;
  background: linear-gradient(to bottom, #78B8DE, #B4E7FF);
  .left-telegram{
    margin-right: 20px;
    margin-bottom: 20px;
    .hub-content{
      text-align:right;
    }
  }
  .right-telegram{
    margin-top: 6%;
    display: flex;
    justify-content: space-around;
    flex-flow: wrap;
    align-items: center;
  }
  .nation{
      font-size:14px;
      text-align: center;
    }
    .img-head{
      height: 4rem;
      width: 4rem;
      border-radius: 2.5rem;
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
