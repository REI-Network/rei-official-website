<template>
  <div class="ecosystem-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
      </div>
  </div>
</template>

<script>
export default {
  name: 'EcosystemPage',
  data() {
    return {
      banner: require('@/assets/img/ecosystem/banner.png')
    }
  },
}
</script>
