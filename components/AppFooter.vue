<template>
  <div id="footer">
    <v-divider></v-divider>
    <Subscribe></Subscribe>
    <v-divider  class="mt-12"></v-divider>
    <v-container class="align-center">
      <v-row
        class="mt-16"
      >
        <v-col cols="12" md="3" lg="3">
          <div class="footer-title font-weight-black"><logo /></div>
          <div class="footer-text2 mt-3">
            REI Network is A New,Lightweight And
            Quasi-Free Application-Level Public Chain
            That is EVM-Compatible And is More
            Friendly To Developers.
          </div>
        </v-col>
        <v-col cols="12" md="9" lg="9">
          <v-row>
            <v-col
              v-for="item in project"
              :key="item.name"
              cols="12"
              lg="2"
              md="2"
              class="d-flex flex-column"
            >
              <div class="ml-2 mb-4 font-weight-black subtitle-2">{{ item.name }}</div>
              <div v-for="link in item.list" :key="link.name">
                <v-btn
                  :to="link.to"
                  :href="link.href"
                  :target="link.target"
                  plain
                  text
                  nofollow
                  x-small
                >
                  {{ link.name }}
                </v-btn>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <v-divider  class="mt-12"/>
    <v-container>
      <v-row justify="space-between">
        <div class="copy-center">&copy; 2022 REI Network</div>
        <div class="copy-center">Privacy Policy</div>
      </v-row>
    </v-container>
  </div>
</template>
<script>
import Logo from '../components/Logo.vue'
import Subscribe from './Subscribe.vue';
export default {
  data() {
    return {
      email: '',
      loading: false,
      disabled: true,
      subSuccessShow: false,
      project: [
        {
          name: 'Developer',
          list: [
            {
              name: 'Get Started',
              to: '/',
            },
            {
              name: 'Dev Docs',
              href: '/',
              target: '_blank',
            },
            {
              name: 'Bug Bounty',
              to: '/',
            },
            {
              name: 'Chat On Discord',
              to: '/',
            },
          ],
        },
        {
          name: 'USE REI',
          list: [
            {
              name: 'Ecosystem',
              to:'/ecosystem'
            },
            {
              name: 'REI EXplorer',
              to: '/',
            }
          ],
        },
        {
          name: 'REIcosystem',
          list: [
            {
              name: 'Introduction',
              href: '',
              target: '_blank',
            },
            {
              name: 'Apply For Grants',
              to: '/',
            }
          ],
        },
        {
          name: 'REI DAO',
          list: [
            {
              name: 'Dashboard',
              to: '/',
            },
            {
              name: 'My Account',
              to: '/',
            },
            {
              name: 'Voting',
              to: '/',
            }
          ],
        },
        {
          name: 'Media',
          list: [
            {
              name: 'Blogs',
              to: '/',
            },
            {
              name: 'General News',
              to: '/',
            },
            {
              name: 'Brand Kits',
              to: '/',
            },
          ],
        },
        {
          name: 'Community',
          list: [
            {
              name: 'Hub',
              to: '/',
            },
            {
              name: 'Subscribe',
              to: '/',
            }
          ],
        },
      ],
    }
  },
  components:{
    Subscribe
  }
}
</script>
<style scoped>
#footer {
  padding-top: 18px;
}
.align-center{
  max-width: 1220px;
}
.footer-title {
  font-size: 28px;
}
.footer-text {
  font-size: 18px;
  color: #b1b6bb;
}
.footer-text2 {
  font-size: .8rem;
  color: #b1b6bb;
}

.copy-center {
  padding: 30px 0;
  text-align: center;
  color: #b1b6bb;
}
</style>
