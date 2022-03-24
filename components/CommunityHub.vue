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
                  <v-img :src="twitter" height="180" width="160" />
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
                  class="hub-background mt-6 reddit"
                  >
                  <img :src="reddit" height="180" width="160" />
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
                  <img :src="github" height="180" width="160" />
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
                  class="hub-background mt-6 kakao"
                  >
                  <img :src="talk" height="180" width="160" />
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
                  <v-img :src="discord" height="260" width="280" class="discord-img"/>
                  <div class="hub-content">
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
                  <img :src="Telegram" height="180" width="180" />
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
                    <img src="@/assets/img/community/EnglishCommunity.png" alt="" class="img-head">
                    <div>English</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/KoreanCommunity.png" alt="" class="img-head">
                    <div>Korean</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/RussianCommunity.png" alt="" class="img-head">
                    <div>Russian</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/SpanishCommunity.png" alt="" class="img-head">
                    <div>Spanish</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/GermanCommunity.png" alt="" class="img-head">
                    <div>German</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/JapaneseCommunity.png" alt="" class="img-head">
                    <div>Japanese</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/BrazilCommunity.png" alt="" class="img-head">
                    <div>Brazil</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/ItlianCommunity.png" alt="" class="img-head">
                    <div>Itlian</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/VietnameseCommunity.png" alt="" class="img-head">
                    <div>Vietnamese</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/AfricanCommunity.png" alt="" class="img-head">
                    <div>African</div>
                    <div>Community</div>
                  </div>

                  <div class="nation">
                    <img src="@/assets/img/community/TurkishCommunity.png" alt="" class="img-head">
                    <div>Turkish</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/SriLankaCommunity.png" alt="" class="img-head">
                    <div>SriLanka</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/IndonesianCommunity.png" alt="" class="img-head">
                    <div>Indonesian</div>
                    <div>Community</div>
                  </div>
                  <div class="nation">
                    <img src="@/assets/img/community/FrenchCommunity.png" alt="" class="img-head">
                    <div>French</div>
                    <div>Community</div>
                  </div>
              </v-row>
            </v-col>
          </v-row>
            <v-row class="learn-join mt-16" justify="space-around" align="center">
              <div><v-img :src="banner" :aspect-ratio="10/9" width="100" class="img-style"/></div>
              <div class="bounty">
                <h3 class="font-gradient">$1,500,000 For Bug Bounty!#REI #Mainnet</h3>
                <p class="font-white distance">If Ypu Find A Bug Or Have Any Ideas Which Will Improve Mainnet Security.Piz Contact Us</p>
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
             </v-row>
        </v-col>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      twitter:require('@/assets/img/community/twitter.png'),
      reddit:require('@/assets/img/community/reddit.png'),
      github:require('@/assets/img/community/github.png'),
      talk:require('@/assets/img/community/talk.png'),
      discord:require('@/assets/img/community/discord.png'),
      Telegram:require('@/assets/img/community/tg.png'),
      banner: require('@/assets/img/community/REIStartanode.png')
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
    padding:1.2rem 2rem 0 0;
    .hub-content{
      margin-top:1rem;
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
    height: 45.5rem;
    background: linear-gradient(to bottom, #8A92CE, #B6C5F5);
    .discord-img{
      margin-top: 60px;
    }
    .hub-content{
      margin-top: 14rem;
    }

    h2{
      margin: 12px 0;
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
    margin-top: 4%;
    display: flex;
    justify-content: space-around;
    flex-flow: wrap;
    align-items: center;
  }
  .nation{
      font-size:14px;
      text-align: center;
      // background: pink;
      padding: 10px 12px;
    }
    .img-head{
      height: 4rem;
      width: 4rem;
      border-radius: 2.5rem;
    }
    .nation:hover{
      background-color: rgba(255,255,255,0.6);
      border-radius: 6px;
      color: #000;
    }
}

.learn-join{
  // padding: 20px;
  background: linear-gradient(to bottom right, #3E1D8C, #715FA3);
  .img-style{
    margin: 20px 0;
  }
  .img-style-learn{
    width: 4.6rem;
    height: 6.8rem;
  }
  .tow-btn{
    display: flex;
    flex-direction: column;
  }
  .bounty{
     margin-top: 12px;
  }
  .distance{
    margin-top: 12px;
  }
  .btn-background{
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
