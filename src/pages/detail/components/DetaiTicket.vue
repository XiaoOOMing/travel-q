<template>
  <div class="d-ticket" ref="tagTop">
    <div class="tag border-bottom">
      <div class="item" :class="{active: tag}" ref="ticket">门票</div>
      <div class="item" :class="{active: !tag}" ref="oneDay">一日游</div>
    </div>
    <div class="ticket-item">
      <div class="head-title border-bottom">
        <i class="iconfont">&#xe659;</i>
        <span>中秋日场活动票</span>
      </div>
      <div class="item border-bottom">
        <div class="item-title">成人票</div>
        <div class="item-price">
          <span class="price-wrapper">
            <span class="orange">￥<span class="price">98</span></span>
          起
          </span>
          <i class="iconfont">&#xe695;</i>
        </div>
      </div>
      <div class="item border-bottom">
        <div class="item-title">大学生票</div>
        <div class="item-price">
          <span class="price-wrapper">
            <span class="orange">￥<span class="price">58</span></span>
          起
          </span>
          <i class="iconfont">&#xe695;</i>
        </div>
      </div>
    </div>
    <div class="ticket-item">
      <div class="head-title border-bottom">
        <i class="iconfont">&#xe659;</i>
        <span>中秋日场活动票</span>
      </div>
      <div class="item border-bottom">
        <div class="item-title">成人票</div>
        <div class="item-price">
          <span class="price-wrapper">
            <span class="orange">￥<span class="price">98</span></span>
          起
          </span>
          <i class="iconfont">&#xe695;</i>
        </div>
      </div>
      <div class="item border-bottom">
        <div class="item-title">大学生票</div>
        <div class="item-price">
          <span class="price-wrapper">
            <span class="orange">￥<span class="price">58</span></span>
          起
          </span>
          <i class="iconfont">&#xe695;</i>
        </div>
      </div>
    </div>
    <div class="ticket-item">
      <div class="head-title border-bottom">
        <i class="iconfont">&#xe659;</i>
        <span>中秋日场活动票</span>
      </div>
      <div class="item border-bottom">
        <div class="item-title">成人票</div>
        <div class="item-price">
          <span class="price-wrapper">
            <span class="orange">￥<span class="price">98</span></span>
          起
          </span>
          <i class="iconfont">&#xe695;</i>
        </div>
      </div>
      <div class="item border-bottom">
        <div class="item-title">大学生票</div>
        <div class="item-price">
          <span class="price-wrapper">
            <span class="orange">￥<span class="price">58</span></span>
          起
          </span>
          <i class="iconfont">&#xe695;</i>
        </div>
      </div>
    </div>
    <div ref="oneDayAnchor"></div>
    <div class="ticket-item">
      <div class="head-title border-bottom">
        <i class="iconfont">&#xe659;</i>
        <span>一日游</span>
      </div>
      <div class="item border-bottom">
        <div class="item-title">【天津触发】北京欢乐谷1日游</div>
        <div class="item-price">
          <span class="price-wrapper">
            <span class="orange">￥<span class="price">98</span></span>
          起
          </span>
          <i class="iconfont">&#xe695;</i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetaiTicket',
  data () {
    return {
      tag: true
    }
  },
  mounted () {
    this.bindEvents()
    window.addEventListener('scroll', this.tagPosition)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.tagPosition)
  },
  methods: {
    // DOM事件绑定
    bindEvents () {
      const _this = this
      // 点击一日游
      this.$refs.oneDay.onclick = function () {
        let scrollTop = _this.$refs.oneDayAnchor.offsetTop - 88
        window.scrollTo(0, scrollTop)
        _this.tag = false
      }
      // 点击门票
      this.$refs.ticket.onclick = function () {
        let scrollTop = _this.$refs.tagTop.offsetTop - 44
        window.scrollTo(0, scrollTop)
        _this.tag = true
      }
    },
    // 门票 一日游固定在顶部
    tagPosition () {
      let tagTop = this.$refs.tagTop.offsetTop - 44
      let scrollTop = document.body.scrollTop === 0 ? document.documentElement.scrollTop : document.body.scrollTop
      if (tagTop < scrollTop) {
        this.$refs.tagTop.classList.add('fixed')
      } else {
        this.$refs.tagTop.classList.remove('fixed')
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  html, body
    transition all .3s
  .d-ticket
    margin-top .2rem
    &.fixed
      padding-top .88rem
      .tag
        position fixed
        z-index 99
        background-color #fff
        top .88rem
    .tag
      background #fff
      display flex
      width 100%
      .item
        position relative
        text-align center
        line-height .92rem
        width 50%
        font-size .32rem
        color #333
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
      margin-bottom .2rem
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
      .item
        height .96rem
        display flex
        align-items center
        justify-content space-between
        padding 0 .2rem
        color #444
        .item-title
          font-size .30rem
        .item-price
          color #999
          .orange
            color $orange
            .price
              font-size .36rem
</style>
