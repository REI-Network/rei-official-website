<template>
  <div id="footer">
    <v-container class="align-center">
        <v-divider color="#8A8A9A" class="divider"></v-divider>
        <Subscribe></Subscribe>
        <v-divider color="#8A8A9A" class="mt-6 divider"></v-divider>
      <v-row
        class="mt-8"
      >
        <v-col cols="12" md="4" lg="4">
          <div class="footer-title font-weight-black"><logo /></div>
          <div class="footer-text2 mt-3">
            REI Network was developed to better adapt to the development trend of the blockchain, and to achieve a lightweight, Ethereum compatible, higher performance, and no fee blockchain framework.
          </div>
        </v-col>
        <v-col cols="12" md="8" lg="8">
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
                  style="font-size:13px;"
                >
                  {{ link.name }}
                </v-btn>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-divider  color="#8A8A9A" class="mt-8 divider"/>
    </v-container>
    <v-container class="align-center">
      <v-row justify="space-between">
        <div class="copy-center">&copy; 2022 REI Network</div>
        <a href="https://static.rei.network/media/privacy-policy.pdf" target="_blank" class="copy-center">Privacy Policy</a>
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
              to: '/getStarted',
            },
            {
              name: 'Dev Docs',
              href: 'https://docs.rei.network/rei-network/welcome-to-rei-network',
              target: '_blank',
            },
            {
              name: 'Bug Bounty',
              href: 'https://docs.google.com/forms/d/e/1FAIpQLSdW0tOt5nDVlCZw4auUWW0BrfqxujpV6Y_jJt-ilZsGS4sWOQ/viewform',
              target:'_blank'
            },
            {
              name: 'Chat On Discord',
              href: 'https://discord.com/invite/zhwWkXYtJt',
              target:'_blank'
            },
          ],
        },
        {
          name: 'Network',
          list: [
            {
              name: 'Ecosystem',
              to:'/reiuse'
            },
            {
              name: 'REI Explorer',
              href: 'https://scan.rei.network/',
              target:'_blank'
            }
          ],
        },
        {
          name: 'REIcosystem',
          list: [
            {
              name: 'Introduction',
              href: 'https://medium.com/gxchain-project/rei-reicosystem-started-150-million-rei-growth-fund-for-ecosystem-building-bcb78658e506',
              target: '_blank',
            },
            {
              name: 'Apply For Grants',
              href: 'https://form.typeform.com/to/q7cU4ewA',
              target:'_blank'
            }
          ],
        },
        {
          name: 'REI DAO',
          list: [
            {
              name: 'Dashboard',
              href: 'https://dao.rei.network/#/dashboards',
              target:'_blank'
            },
            {
              name: 'My Account',
              href: 'https://dao.rei.network/#/myAccount',
              target:'_blank'
            },
            {
              name: 'Voting',
              href: 'https://dao.rei.network/#/stake',
              target:'_blank'
            },
            {
              name: 'Governance',
              href: 'https://dao.rei.network/#/governance',
              target:'_blank'
            },
            {
              name: 'Forum',
              href: 'https://forum.rei.network/',
              target:'_blank'
            }
          ],
        },
        {
          name: 'Media',
          list: [
            {
              name: 'Blogs',
              href: 'https://medium.com/gxchain-project',
              target:'_blank'
            },
            {
              name: 'General News',
              href: 'https://twitter.com/GXChainGlobal',
              target:'_blank'
            },
            {
              name: 'Brand Kits',
              href: 'https://static.rei.network/media/REI-VIS-Basic-System.zip',
            },
          ],
        },
        {
          name: 'Community',
          list: [
            {
              name: 'Hub',
              to: '/community',
            },
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
<style scoped lang="scss">
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
  color: #8A8A9A ;
}
.footer-text2 {
  line-height: 24px;
  font-size: 14px;
  color: #8A8A9A ;
}

.copy-center {
  padding-bottom: 12px ;
  text-align: center;
  color: #8A8A9A ;
  font-size: 14px;
  margin: 0 12px;
}
.divider{
  opacity: 0.15;
}
a{
  text-decoration: none;
}
a:hover{
  text-decoration: underline;
  color: #8A8A9A ;
}
</style>
n
