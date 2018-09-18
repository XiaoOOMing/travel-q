<template>
  <div class="d-info">
    <div class="intro-wrapper">
      <router-link to="/" tag="div" class="item border-right">
        <div class="title orange">
          <span class="score">5.0</span>分 超赞
        </div>
        <div class="desc">
          559975条评论
          18条攻略
        </div>
        <i class="iconfont">&#xe65e;</i>
      </router-link>
      <router-link to="/" tag="div" class="item">
        <div class="title">
          景点介绍
        </div>
        <div class="desc">
          开发时间 贴士
        </div>
        <i class="iconfont">&#xe65e;</i>
      </router-link>
    </div>
    <router-link to="/" tag="div" class="address-wrapper border-top">
      <i class="iconfont">&#xe64e;</i>
      <span class="title">北京市朝阳区东四环小武基北路</span>
      <i class="iconfont">&#xe65e;</i>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'DetailInfo'
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .d-info
    background-color #fff
    border-top-left-radius .15rem
    border-top-right-radius .15rem
    overflow hidden
    transform: translateY(-.1rem)
    margin-bottom .1rem
    .intro-wrapper
      display flex
      padding .2rem 0
      .item
        padding-left .3rem
        width 50%
        position relative
        i
          color #999
          position absolute
          right .1rem
          top 50%
          transform translateY(-50%)
        .title
          height .48rem
          line-height .48rem
          margin-bottom .05rem
          color #222
          &.orange
            color $orange
            .score
              font-size .40rem
        .desc
          color #999
          font-size .24rem
    .address-wrapper
      line-height .72rem
      display flex
      justify-content space-between
      i
        color #999
        width .55rem
        height .72rem
        text-align center
      .title
        flex 1
</style>
