<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content"></div>
  </div>
</template>
<script>
import DetailBanner from './components/banner.vue'
import DetailHeader from './components/header.vue'
export default {
  name: 'detail',
  components: {
    DetailBanner,
    DetailHeader
  }
}
</script>
<style lang='stylus' socped>
  .content
    height: 50rem
</style>
