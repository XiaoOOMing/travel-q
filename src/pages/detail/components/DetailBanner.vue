<template>
  <div class="d-banner">
    <img src="//img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_600x330_93d96bdf.jpg">
    <div class="info">
      <div class="img-num">
        <i class="iconfont">&#xe626;</i>
        <span>16</span>
      </div>
      <div class="title">北京欢乐谷(AAAA景区)</div>
      <div class="bg"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailBanner'
}
</script>

<style lang="stylus" scoped>
  .d-banner
    position relative
    width 100%
    overflow hidden
    img
      width 100%
    .info
      position absolute
      bottom 0
      left 0
      width 100%
      padding .45rem .2rem
      .bg
        display: block;
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        min-height: .6rem;
        background-color: transparent;
        background-image: linear-gradient(to bottom,rgba(0,0,0,0),rgba(0,0,0,.8))
      .img-num
        font-size .24rem
        display inline-block
        background rgba(0,0,0,0.6)
        color #fff
        padding 0 .25rem
        line-height .4rem
        border-radius .2rem
        margin-bottom .1rem
        i
          font-size .28rem
      .title
        position relative
        text-shadow 0 1px 2px rgba(0,0,0,0.70)
        color #fff
        font-size .35rem
</style>
