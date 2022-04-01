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
           <v-list  v-if="item.system">
              <v-list-item link to="/reiuse">
                  <v-list-item-title>{{ item.system }}</v-list-item-title>
              </v-list-item>
              <v-list-item link href="https://scan.rei.network/" target="_blank">
                  <v-list-item-title>{{ item.rei }}</v-list-item-title>
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
          <v-list-item
            v-else
            :key="item.text"
            nuxt
            :to="item.link"
            :href="item.href"
            :target="item.target"
          >
            <v-list-item-title>
              <span>
                {{ item.text }}
              </span>
            </v-list-item-title>
          </v-list-item>

        </template>
        <v-list-item
            nuxt
            to="/getStarted"
          >
            <v-list-item-title>
              <span>
                Get Started
              </span>
            </v-list-item-title>
          </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <app-footer />
  </v-app>
</template>

<script>
import { mdiMenu,mdiChevronDown } from '@mdi/js'
import Logo from '../components/Logo.vue'
import AppFooter from '../components/AppFooter.vue'
export default {
  name: 'DefaultLayout',
  components: { Logo, AppFooter },
  data () {
    return {
      mdiMenu,
      mdiChevronDown,
      showDrawer: false,
      links: [
        {
          text: 'Developer',
          link: '/developer',
        },
        {
          text: 'Network',
          system:'Ecosystem',
          rei:'REI Explorer'

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
      rightDrawer: false,
      title: 'Vuetify.js'
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
</style>
