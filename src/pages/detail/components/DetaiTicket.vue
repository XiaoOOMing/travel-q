<template>
  <div class="d-ticket">
    <div class="tag border-bottom">
      <div class="item active">门票</div>
      <div class="item">一日游</div>
    </div>
    <div class="ticket-item">
      <div class="head-title">
        <i class="iconfont">&#xe659;</i>
        <span>日场活动票</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetaiTicket'
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .d-ticket
    margin-top .2rem
    .tag
      background #fff
      display flex
      .item
        position relative
        text-align center
        line-height .92rem
        width 50%
        font-size .32rem
        &.active::before
          content ' '
          position absolute
          bottom 0
          left 50%
          transform translateX(-50%)
          width 40%
          border-bottom 2px solid $bgColor
    .ticket-item
      background #fff
      .head-title
        line-height .92rem
        padding-left .2rem
        font-size .32rem
        color #333
        i
          display inline-block
          width .4rem
          height .4rem
          line-height .4rem
          border-radius .4rem
          font-size .24rem
          text-align center
          background-color $bgColor
          color #fff
          transform rotate(35deg)
</style>
