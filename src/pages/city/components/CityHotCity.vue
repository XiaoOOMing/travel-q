<template>
  <div class="c-hot-city">
    <div class="title">热门城市</div>
    <div class="li-wrapper">
      <div class="lines"></div>
      <div class="li-item">北京</div>
      <div class="li-item">上海</div>
      <div class="li-item">三亚</div>
      <div class="li-item">香港</div>
      <div class="li-item">杭州</div>
      <div class="li-item">广州</div>
      <div class="li-item">成都</div>
      <div class="li-item">深圳</div>
      <div class="li-item">苏州</div>
      <div class="li-item">桂林</div>
      <div class="li-item">西安</div>
      <div class="li-item">厦门</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityHotCity'
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .c-hot-city
    .title
      font-size .24rem
      line-height $topHeigth
      padding 0 .2rem
    .li-wrapper
      position relative
      background #fff
      display flex
      flex-wrap wrap
      justify-content flex-start
      .lines
        position absolute
        width calc(100% / 3)
        height 100%
        border-left 1px solid #eee
        border-right 1px solid #eee
        top 0
        left calc(100% / 3)
      .li-item
        width calc(100% / 3)
        text-align center
        line-height $topHeigth
        border-bottom 1px solid #eee
</style>
