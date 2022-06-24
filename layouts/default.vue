<template>
  <v-app light>
    <v-app-bar
      fixed
      app
      color="#FFF"
      height="80"
      elevation="0"
      class="header"
    >
      <v-container class="d-flex align-center" style="max-width:1220px;padding:0;">
        <v-btn text color="transparent" to="/" style="padding:0">
          <logo />
        </v-btn>
         <v-spacer />
        <v-menu
          v-for="item in links"
          :key="item.text"
          open-on-hover
          bottom
          transition="slide-y-transition"
          offset-y
        >
          <template #activator="{ on, attrs }">
            <v-btn
              class="hidden-sm-and-down nav-btn text-subtitle-1"
              plain
              nuxt
              replace
              :to="item.link"
              :href="item.href"
              :target="item.target"
              :ripple="false"
              v-bind="attrs"
              v-on="on"
            >
              <v-img
                v-if="item.icon"
                contain
                width="90"
                :src="item.icon"
                alt=""
              />
              <span v-else>
                {{ item.text }}
                <v-icon v-if="item.childs">{{ mdiChevronDown }}</v-icon>
              </span>
            </v-btn>
          </template>
           <v-list class="network-list" v-if="item.system" two-line>
              <v-list-item link to="/reiuse" class="network-item">
                <v-list-item-avatar>
                  <v-img :src="item.avatar"></v-img>
                </v-list-item-avatar>
                  <v-list-item-content>
                    <v-list-item-title>{{ item.system }}</v-list-item-title>
                    <v-list-item-subtitle class="subtitle">Explore the latest projects on REI Network</v-list-item-subtitle>
                  </v-list-item-content>
              </v-list-item>
              <v-list-item link href="https://scan.rei.network/" target="_blank" class="network-item">
                <v-list-item-avatar>
                  <v-img :src="item.avatar1"></v-img>
                </v-list-item-avatar>
                <v-list-item-content>
                  <v-list-item-title>{{ item.rei }}</v-list-item-title>
                  <v-list-item-subtitle class="subtitle">Explore the REI Network transactions, blocks, and more info</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
              <v-list-item target="_blank" class="network-item">
                <v-list-item-avatar>
                  <v-img :src="item.avatar2"></v-img>
                </v-list-item-avatar>
                <v-list-item-content>
                  <v-list-item-title>Bridges</v-list-item-title>
                  <v-list-item-subtitle class="subtitle">
                     <v-row justify="space-between">
                       <v-col><a href="https://app.multichain.org/#/router" target="_blank" >Multichain ></a></v-col>
                       <v-col><a href="https://cbridge.celer.network/#/transfer" target="_blank" >Cbridge ></a></v-col>
                       <!-- <v-col><a href="https://scan.rei.network/" target="_blank" >Dashboard ></a></v-col> -->
                     </v-row>
                  </v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          <v-list v-if="item.childs">
            <v-list-item v-for="child in item.childs" :key="child.text">
              <v-btn
                class="hidden-sm-and-down nav-btn text-subtitle-1"
                plain
                nuxt
                :to="child.link"
                :href="child.href"
                :target="child.target"
                :ripple="false"
              >
                <span>
                  {{ child.text }}
                </span>
              </v-btn>
            </v-list-item>
          </v-list>

        </v-menu>
        <v-btn
            small
            class="hidden-sm-and-down nav-btn text-subtitle-1 left-margin"
            color="#1D10F8"
            height="44"
            dark
            to="/getStarted"
        >
            Get Started
        </v-btn>
        <v-btn
          class="hidden-md-and-up"
          text
          icon
          @click.stop="showDrawer = !showDrawer"
        >
          <v-icon>{{ mdiMenu }}</v-icon>
        </v-btn>
      </v-container>
    </v-app-bar>
    <v-main>
        <Nuxt />
    </v-main>
   <v-navigation-drawer v-model="showDrawer" right temporary fixed>
      <v-list>
        <template v-for="item in links">
          <v-list-group v-if="item.childs" :key="item.text" no-action>
            <template #activator>
              <v-list-item-title>{{ item.text }}</v-list-item-title>
            </template>
            <v-list-item
              v-for="child in item.childs"
              :key="child.text"
              nuxt
              :to="child.link"
              :href="child.href"
              :target="child.target"
            >
              <v-list-item-title>
                <span>
                  {{ child.text }}
                </span>
              </v-list-item-title>
            </v-list-item>
          </v-list-group>
          <v-list-group
            v-else
            :key="item.text"
            nuxt
            :value="true"
            no-action
          >
          <template #activator>
            <v-list-item :to="item.link" :href="item.href" :target="item.target">
              <v-list-item-title>
                <span>
                  {{ item.text }}
                </span>
            </v-list-item-title>
            </v-list-item>
          </template>
            <v-list-item-content v-if="item.system">
              <v-list-item class="left-margin" link to="/reiuse">
                  <v-list-item-subtitle>{{ item.system }}</v-list-item-subtitle>
              </v-list-item>
              <v-list-item  class="left-margin" link href="https://scan.rei.network/" target="_blank">
                  <v-list-item-subtitle>{{ item.rei }}</v-list-item-subtitle>
              </v-list-item>
            </v-list-item-content>
          </v-list-group>
        </template>
        <v-list-item
            nuxt
            to="/getStarted"
          >
            <v-list-item-title class="left-margin">
              <span>
                Get Started
              </span>
            </v-list-item-title>
          </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <app-footer />
    <div class="scroll-top" @click="backTop()" v-show="backFlag">
        <v-icon
            x-large
            color="#1d10f8"
          >
          {{mdiChevronUp}}
        </v-icon>
      </div>
  </v-app>
</template>

<script>
import { mdiMenu,mdiChevronDown,mdiChevronUp } from '@mdi/js'
import Logo from '../components/Logo.vue'
import AppFooter from '../components/AppFooter.vue'
export default {
  name: 'DefaultLayout',
  components: { Logo, AppFooter },
  data () {
    return {
      mdiMenu,
      mdiChevronDown,
      mdiChevronUp,
      showDrawer: false,
      links: [
        {
          text: 'Developer',
          link: '/developer',
        },
        {
          text: 'Network',
          system:'Ecosystem',
          rei:'REI Explorer',
          avatar:require("../assets/img/Ecosystem.png"),
          avatar1:require("../assets/img/REI Explore.png"),
          avatar2:require("../assets/img/Chain Bridge.png")
        },
        {
          text: 'REIcosystem',
          link: '/ecosystem'
        },
        {
          text: 'Media',
          link: '/media',
        },
        {
          text: 'Community',
          link: '/community',
        },
        {
          text: 'REI DAO',
          href: 'https://dao.rei.network',
          target: '_blank',
        }
      ],
      miniVariant: false,
      right: true,
      backFlag:false,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  },
  mounted () {
      let that = this;
      window.addEventListener('scroll', that.scrollToTop);
      this.scrollToTop ()
    },

  destroyed (){
      let that = this;
      window.removeEventListener('scroll', that.scrollToTop);
      this.scrollToTop ()
  },
  methods:{
    backTop () {
      let timer = setInterval(function () {
        var top = document.body.scrollTop || document.documentElement.scrollTop;
        var speed = top / 4;
        if (document.body.scrollTop!=0) {
          document.body.scrollTop -= speed;
        }else {
          document.documentElement.scrollTop -= speed;
        }
        if (top == 0) {
          clearInterval(timer);
        }
      },30);
    },
    scrollToTop () {
      const that = this
      let scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop
      that.scrollTop = scrollTop;
      if (that.scrollTop > 100) {
        that.backFlag = true
      }else {
        that.backFlag = false
      }
    }
  }
}
</script>
<style scoped lang="scss">
.header{
  box-shadow: 0 2px 5px 1px rgb(64 60 67 / 16%) !important;
  /* filter: blur(20px);
  opacity: 0.8; */
}
.left-margin{
  margin-left: 16px;
}
.v-btn.v-btn--has-bg{
  background-color: transparent;
}
.network-list{
  width: 470px;
  padding-bottom: 20px;
  margin-top:20px;
  // box-shadow: 0 0 20px #ddd !important;
  .network-item{
    padding: 12px 28px;
  }
  .subtitle{
    margin-top:8px;
  }
}
.scroll-top{
  position:fixed;
  right:28px;
  bottom:120px;
  border-radius: 50px;
  border: 1px #E2E2E2 solid;
  padding:10px;
  cursor: pointer;
}
a{
  text-decoration: none;
  color: #7E7E7E;
}
a:hover{
  text-decoration: underline;
  // color: #6979f8;
}
</style>
