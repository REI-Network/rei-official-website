<template>
  <div class="media-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
      </div>
  </div>
</template>

<script>
export default {
  name: 'MediaPage',
  data() {
    return {
      banner: require('@/assets/img/media/banner.png')
    }
  },
}
</script>
