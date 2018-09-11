<template>
  <div class="c-header">
    <router-link to="/" class="back"><i class="iconfont">&#xe624;</i></router-link>
    <span class="title">城市选择</span>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .c-header
    background $bgColor
    text-align center
    position relative
    line-height $topHeigth
    color #fff
    .back
      position absolute
      width $topHeigth
      height $topHeigth
      line-height $topHeigth
      text-align center
      left 0
      right 0
      color #fff
      .iconfont
        font-weight bold
        font-size .34rem
    .title
      font-size .32rem
</style>
