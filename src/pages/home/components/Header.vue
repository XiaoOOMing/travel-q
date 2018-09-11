<template>
  <div class="header">
    <div class="header-left">
      <i class="iconfont">&#xe624;</i>
    </div>
    <div class="header-input">
      <i class="iconfont">&#xe632;</i>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        北京
        <i class="iconfont">&#xe64a;</i>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .header
    background $bgColor
    height $topHeigth
    line-height $topHeigth
    display flex
    justify-content flex-start
    align-items center
    color #fff
    .header-left
      width .4rem
      padding 0 .2rem
      .iconfont
        font-weight bold
    .header-right
      padding 0 .2rem
      color #fff
      text-decoration none
      .iconfont
        display inline-block
        font-size .24rem
        transform scaleY(.8)
    .header-input
      flex 1
      background #fff
      height .6rem
      line-height .6rem
      color #ddd
      font-size .26rem
      border-radius .05rem
      padding 0 .2rem
</style>
