<template>
  <div id="footer">
    <v-container class="align-center">
      <v-row
        class="mt-16"
        :class="{ 'text-center': $vuetify.breakpoint.smAndDown }"
      >
        <v-col cols="12" md="4" lg="4">
          <div class="footer-titele font-weight-black"><logo /></div>
          <div class="footer-text2 mt-3">
            REI Network is A New,Lightweight And
            Quasi-Free Application-Level Public Chain
            That is EVM-Compatible And is More 
            Friendly To Developers.
          </div>
        </v-col>
        <v-col cols="12" md="8" lg="8">
          <v-row>
            <v-col
              v-for="item in project"
              :key="item.name"
              cols="3"
              lg="3"
              md="3"
              class="d-flex flex-column"
            >
              <div class="ml-4 mb-4 text-h6">{{ item.name }}</div>
              <div v-for="link in item.list" :key="link.name">
                <v-btn
                  :to="link.to"
                  :href="link.href"
                  :target="link.target"
                  plain
                  text
                  nofollow
                >
                  {{ link.name }}
                </v-btn>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <v-divider></v-divider>
    <v-container>
      <div class="copy-center">&copy; 2022 REI Network</div>
    </v-container>
  </div>
</template>
<script>
import Logo from '../components/Logo.vue'
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
  }
}
</script>
<style scoped>
#footer {
  padding-top: 88px;
}
.footer-titele {
  font-size: 28px;
}
.footer-text {
  font-size: 18px;
  color: #b1b6bb;
}
.footer-text2 {
  max-width: 460px;
  font-size: 16px;
  color: #b1b6bb;
}

.copy-center {
  padding: 30px 0;
  text-align: center;
  color: #b1b6bb;
}
</style>
