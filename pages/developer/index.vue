<template>
  <div class="developer-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
      </div>
  </div>
</template>

<script>
export default {
  name: 'DeveloperPage',
  data() {
    return {
      banner: require('@/assets/img/developer/banner.png')
    }
  },
}
</script>
