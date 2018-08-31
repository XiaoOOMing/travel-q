<template>
  <div class="home-adv">
    <div class="item border-right">
      <img src="http://img1.qunarzz.com/piao/fusion/1806/29/30427c0e0658b502.png" class="item-image">
    </div>
    <div class="item">
      <img src="http://img1.qunarzz.com/piao/fusion/1808/84/887ec92cae51f302.png" class="item-image">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeAdv'
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .home-adv
    margin-top $marginTop
    background #fff
    display flex
    .item
      width 50%
      height 0
      padding 0 .25rem
      padding-bottom 18.67%
      background #fff
      overflow hidden
      .item-image
        width 100%
</style>
