<template>
  <div class="community-page">
      <div class="pos-r">
          <v-img :src="banner" height="480" />
      </div>
  </div>
</template>

<script>
export default {
  name: 'CommunityPage',
  data() {
    return {
      banner: require('@/assets/img/community/banner.png')
    }
  },
}
</script>
