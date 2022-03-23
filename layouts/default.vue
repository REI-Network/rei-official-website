<template>
  <v-app light>
    <v-app-bar
      fixed
      app
      color="white"
      elevation="1"
    >
      <v-container class="d-flex align-center">
        <v-btn text color="transparent" to="/" class="always-active mr-8">
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
            color="primary"
            dark
            to="/getStarted"
        >
            Get Started
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
      </v-list>
    </v-navigation-drawer>
    <app-footer />
  </v-app>
</template>

<script>
import { mdiMenu } from '@mdi/js'
import Logo from '../components/Logo.vue'
import AppFooter from '../components/AppFooter.vue'
export default {
  name: 'DefaultLayout',
  data () {
    return {
      mdiMenu,
      showDrawer: false,
      links: [
        {
          text: 'Developer',
          link: '/developer',
        },
        {
          text: 'REI.DAO',
          href: 'https://dao.rei.network',
          target: '_blank',
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
