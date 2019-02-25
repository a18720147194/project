<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_600x330_b5e86902.jpg">
      <div class="banner-info">
        <div class="banner-title">bibibbibi</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe692;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs='imgs' v-show="showGallary" @close='handleGallaryClose'></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/gallary'
export default {
  name: 'banner',
  components: {
    CommonGallary
  },
  data () {
    return {
      imgs: ['http://img1.qunarzz.com/sight/p0/1605/d4/d4e2dce9d328d5b290.img.jpg_r_800x800_892973df.jpg'],
      showGallary: false
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>
<style lang='stylus' socped>
  .banner
    position: relative
    overflow hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, raba(0,0,0,0), raba(0,0,0,0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        margin-top: .14rem
        padding: 0 .4rem
        line-height: .32rem
        height: .32rem
        border-radius: .2rem
        background: rgba(0,0,0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
