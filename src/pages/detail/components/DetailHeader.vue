<template>
  <div class="detail-header">
    <router-link tag="div" to="/" class="abs" v-show="showAbs">
      <i class="iconfont">&#xe624;</i>
    </router-link>
    <div class="fix" v-show="!showAbs" :style="opacityStyle">
      <router-link to="/" tag="a" class="back">
        <i class="iconfont">&#xe624;</i>
      </router-link>
      <span class="title">北京欢乐谷</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 1
      }
    }
  },
  methods: {
    handleScroll () {
      let scrollTop = document.documentElement.scrollTop
      if (scrollTop === 0) {
        scrollTop = document.body.scrollTop
      }
      if (scrollTop > 0) {
        let opacity = scrollTop / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = {opacity}
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .detail-header
    position absolute
    top 0
    left 0
    width 100%
    height $topHeigth
    z-index 99
    .fix
      position fixed
      top 0
      left 0
      width 100%
      background $bgColor
      height $topHeigth
      line-height $topHeigth
      text-align center
      color #fff
      font-size .32rem
      .back
        position absolute
        left 0
        top 0
        width $topHeigth
        height $topHeigth
        line-height $topHeigth
        text-align center
        color: #fff
        i
          font-weight bold
    .abs
      position absolute
      left .1rem
      top .1rem
      width .72rem
      height .72rem
      line-height .72rem
      text-align center
      border-radius .36rem
      color #fff
      background rgba(0,0,0,0.6)
      i
        font-weight bold
</style>
