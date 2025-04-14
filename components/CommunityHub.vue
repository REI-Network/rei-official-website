<template>
  <div>
    <v-container class="mt-12 align-item">
      <h1>Community Hub</h1>
      <v-row class="font-white mt-4" justify="space-between">
        <v-col cols="12" sm="4">
          <v-hover v-slot="{ hover }" open-delay="200">
            <v-card
              tile
              :elevation="hover ? 12 : 0"
              :class="{ 'on-hover': hover }"
              class="hub-background mt-10 twitter"
            >
              <v-img :src="twitter" height="180" width="180" />
              <div class="hub-content">
                <a href="https://twitter.com/GXChainGlobal" target="_blank">
                  <div class="hub-name font-white">
                    Twitter
                    <img
                      height="8"
                      width="20"
                      style="margin-bottom: 4px"
                      src="../assets/img/arrow_white.png"
                    />
                  </div>
                </a>
                <h2 class="font-white font-bebas">≈ 124,052</h2>
                <div class="font-white">Followers</div>
              </div>
            </v-card>
          </v-hover>
          <v-hover v-slot="{ hover }" open-delay="200">
            <v-card
              tile
              :elevation="hover ? 12 : 0"
              :class="{ 'on-hover': hover }"
              class="hub-background mt-6 reddit"
            >
              <img :src="reddit" height="180" width="160" />
              <div class="hub-content">
                <a a href="https://www.reddit.com/r/GXS/" target="_blank">
                  <div class="hub-name font-white">
                    Reddit
                    <img
                      height="8"
                      width="20"
                      style="margin-bottom: 4px"
                      src="../assets/img/arrow_white.png"
                    />
                  </div>
                </a>
                <h2 class="font-white font-bebas">≈ 27,100</h2>
                <div class="font-white">Members</div>
              </div>
            </v-card>
          </v-hover>
        </v-col>
        <v-col cols="12" sm="4">
          <v-hover v-slot="{ hover }" open-delay="200">
            <v-card
              tile
              :elevation="hover ? 12 : 0"
              :class="{ 'on-hover': hover }"
              class="hub-background mt-10 github"
            >
              <v-img
                :src="github"
                height="300"
                width="240"
                class="discord-img"
              />
              <div class="hub-content">
                <a a href="https://github.com/rei-network" target="_blank">
                  <div class="hub-name font-white">
                    GitHub
                    <img
                      height="8"
                      width="20"
                      style="margin-bottom: 4px"
                      src="../assets/img/arrow_white.png"
                    /></div
                ></a>
              </div>
            </v-card>
          </v-hover>
        </v-col>
        <v-col cols="12" sm="4">
          <v-hover v-slot="{ hover }" open-delay="200">
            <v-card
              tile
              :elevation="hover ? 12 : 0"
              :class="{ 'on-hover': hover }"
              class="hub-background mt-10 discord"
            >
              <v-img
                :src="discord"
                height="289"
                width="312"
                class="discord-img"
              />
              <div class="hub-content">
                <a
                  a
                  href="https://discord.com/invite/zhwWkXYtJt"
                  target="_blank"
                >
                  <div class="hub-name font-white">
                    discord
                    <img
                      height="8"
                      width="20"
                      style="margin-bottom: 4px"
                      src="../assets/img/arrow_white.png"
                    /></div
                ></a>
                <h2 class="font-white font-bebas">≈ 46,801</h2>
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
              <div class="hub-content">
                <a a href="https://t.me/GXChain_international" target="_blank">
                  <div class="hub-telegram font-white">
                    Telegram
                    <img
                      height="8"
                      width="20"
                      style="margin-bottom: 4px"
                      src="../assets/img/arrow_white.png"
                    /></div
                ></a>
                <h2 class="font-white font-bebas">≈ 91,160</h2>
                <div class="font-white">Members</div>
              </div>
            </div>
          </v-col>
          <v-col cols="12" md="8">
            <v-row class="right-telegram" justify="space-around" no-gutters>
              <a
                href="https://t.me/GXChain_international"
                target="_blank"
                class="line-color"
              >
                <div class="nation">
                  <img
                    src="@/assets/img/community/EnglishCommunity.png"
                    alt=""
                    class="img-head"
                  />
                  <div>English</div>
                  <div>Community</div>
                </div>
              </a>
              <a
                href="https://t.me/gxchainkorean"
                target="_blank"
                class="line-color"
              >
                <div class="nation">
                  <img
                    src="@/assets/img/community/KoreanCommunity.png"
                    alt=""
                    width="60"
                    height="54"
                  />
                  <div>Korean</div>
                  <div>Community</div>
                </div>
              </a>
              <!-- <a href="https://t.me/GXChain_Rus" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/RussianCommunity.png" alt="" class="img-head">
                      <div>Russian</div>
                      <div>Community</div>
                    </div>
                  </a>
                  <a href="https://t.me/GXChainhispano" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/SpanishCommunity.png" alt="" class="img-head">
                      <div>Spanish</div>
                      <div>Community</div>
                    </div>
                  </a> -->
              <!-- <a href="https://t.me/GXChainDeutsch" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/GermanCommunity.png" alt="" class="img-head">
                      <div>German</div>
                      <div>Community</div>
                    </div>
                  </a> -->
              <a
                href="https://t.me/GXChainJapanese"
                target="_blank"
                class="line-color"
              >
                <div class="nation">
                  <img
                    src="@/assets/img/community/JapaneseCommunity.png"
                    alt=""
                    class="img-head"
                  />
                  <div>Japanese</div>
                  <div>Community</div>
                </div>
              </a>
              <!-- <a href="https://t.me/GXChainBrazil" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/BrazilCommunity.png" alt="" class="img-head">
                      <div>Brazil</div>
                      <div>Community</div>
                    </div>
                  </a>
                  <a href="https://t.me/GXChainItalia" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/ItlianCommunity.png" alt="" class="img-head">
                      <div>Italian</div>
                      <div>Community</div>
                    </div>
                  </a>
                  <a href="https://t.me/gxchainvietnam" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/VietnameseCommunity.png" alt="" class="img-head">
                      <div>Vietnamese</div>
                      <div>Community</div>
                    </div>
                  </a>
                  <a href="https://t.me/GXChainAfrica" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/AfricanCommunity.png" alt="" class="img-head">
                      <div>African</div>
                      <div>Community</div>
                    </div>
                  </a>
                  <a href="https://t.me/GXChainTurkey" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/TurkishCommunity.png" alt="" class="img-head">
                      <div>Turkish</div>
                      <div>Community</div>
                    </div>
                  </a>
                  <a href="https://t.me/gxchainsrilanka" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/SriLankaCommunity.png" alt="" class="img-head">
                      <div>SriLanka</div>
                      <div>Community</div>
                    </div>
                  </a>
                  <a href="https://t.me/GXChain_Indonesia" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/IndonesianCommunity.png" alt="" class="img-head">
                      <div>Indonesian</div>
                      <div>Community</div>
                    </div>
                  </a>
                  <a href="https://t.me/GXChainFrench" target="_blank" class="line-color">
                    <div class="nation">
                      <img src="@/assets/img/community/FrenchCommunity.png" alt="" class="img-head">
                      <div>French</div>
                      <div>Community</div>
                    </div>
                  </a> -->
            </v-row>
          </v-col>
        </v-row>
        <v-row class="learn-join mt-16" justify="space-around" align="center">
          <div>
            <v-img
              :src="banner"
              :aspect-ratio="13 / 12"
              width="130"
              class="img-style"
            />
          </div>
          <div class="bounty">
            <h3 class="font-gradient">
              150 million $REI Growth Fund for #REIcosystem Building!
            </h3>
            <p class="font-white distance">
              Thank you for applying for the REI Network ecosystem partner.
              Please fill in all details of your proposal in this form.
            </p>
          </div>
          <div class="tow-btn">
            <v-btn
              color="#1D10F8"
              class="btn-background font-white"
              href="https://medium.com/gxchain-project/rei-reicosystem-started-150-million-rei-growth-fund-for-ecosystem-building-bcb78658e506"
              target="_blank"
              width="100"
              height="32"
              depressed
            >
              Learn More
            </v-btn>
            <v-btn
              color="green"
              class="btn-background mt-4 font-white"
              href="https://form.typeform.com/to/q7cU4ewA"
              target="_blank"
              width="100"
              height="32"
              depressed
            >
              Apply
            </v-btn>
          </div>
        </v-row>
      </v-col>
    </v-container>
  </div>
</template>
<script>
import { mdiAtomVariant } from "@mdi/js";
export default {
  data() {
    return {
      twitter: require("@/assets/img/community/twitter.png"),
      reddit: require("@/assets/img/community/reddit.png"),
      github: require("@/assets/img/community/github.png"),
      talk: require("@/assets/img/community/talk.png"),
      discord: require("@/assets/img/community/discord.png"),
      Telegram: require("@/assets/img/community/tg.png"),
      banner: require("@/assets/img/community/REIStartanode.png"),
      arrow: require("@/assets/img/arrow.svg"),
    };
  },
  components: {},
};
</script>

<style lang="scss" scoped>
.align-item {
  max-width: 1220px;
}
.font-bebas {
  font-family: bebas;
}
.font-white {
  color: #fff;
}
a {
  text-decoration: none;
  color: #fff;
}
a:hover {
  text-decoration: underline;
  color: #fff;
}
.on-hover {
  box-shadow: 0 0 20px #ddd !important;
  transform: translateY(-10px);
  transition: transform 0.8s;
}
.line-color:hover {
  color: #000;
}
.hub-background {
  height: 22rem;
  padding: 20px 45px 45px 0;
  .hub-content {
    text-align: right;
  }
}
.twitter {
  background: linear-gradient(to bottom, #1b9be6, #9edfff);
}
.reddit {
  background: linear-gradient(to bottom, #ff744d, #ffa78a);
}
.github {
  background: linear-gradient(to bottom, #7e707e, #b1b3b1);
  height: 45.5rem;
  .discord-img {
    margin-top: 50px;
  }
  .hub-content {
    margin-top: 200px;
  }
  h2 {
    margin: 12px 0;
  }
}
.discord {
  height: 45.5rem;
  background: linear-gradient(to bottom, #8a92ce, #b6c5f5);
  .discord-img {
    margin-top: 50px;
  }
  .hub-content {
    margin-top: 200px;
  }

  h2 {
    margin: 12px 0;
  }
}
.hub-name {
  font-size: 28px;
  font-weight: 900;
}
.hub-telegram {
  font-size: 28px;
  font-weight: 900;
  margin-top: -120px;
}
.telegram {
  font-size: 14px;
  background: linear-gradient(to bottom, #78b8de, #b4e7ff);
  .left-telegram {
    margin-right: 20px;
    margin-bottom: 20px;
    .hub-content {
      text-align: right;
    }
  }
  .right-telegram {
    margin-top: 28px;
    display: flex;
    justify-content: space-around;
    flex-flow: wrap;
    align-items: center;
  }
  .nation {
    font-size: 14px;
    text-align: center;
    // background: pink;
    padding: 10px 16px;
  }
  .img-head {
    height: 54px;
    width: 54px;
    border-radius: 28px;
  }
  .nation:hover {
    background-color: rgba(255, 255, 255, 0.6);
    border-radius: 6px;
    color: #000;
  }
}

.learn-join {
  background: linear-gradient(150deg, #6757a0, #8a7eb5);
  padding: 0 20px;
  .img-style {
    margin: 16px 0;
  }
  .img-style-learn {
    width: 4.6rem;
    height: 6.8rem;
  }
  .tow-btn {
    display: flex;
    flex-direction: column;
    margin-bottom: 12px;
  }
  .bounty {
    margin-top: 12px;
  }
  .distance {
    margin-top: 20px;
    font-size: 15px;
  }
  .btn-background {
    border-radius: 30px;
    font-size: 12px;
  }
  .font-gradient {
    font-size: 25px;
    font-weight: 900;
    background: linear-gradient(to right, #fff0b5, #ffadbf);
    -webkit-background-clip: text;
    color: transparent;
  }
}
.learn-join:hover {
  box-shadow: 0 0 20px #ddd !important;
  transform: translateY(-10px);
  transition: transform 0.8s;
}
</style>
