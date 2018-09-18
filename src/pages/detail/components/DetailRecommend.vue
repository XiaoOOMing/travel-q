<template>
  <div class="d-recommend">
    <div class="header-title border-bottom">
      <i class="iconfont">&#xe650;</i>
      去哪儿推荐
    </div>
    <div class="item">
      <div class="infos">
        <div class="title">北京欢乐谷中秋日场特惠票(同一身份证号及手机号出游日限购1张)</div>
        <div class="time">
          <img class="ticket-tagicon" src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png">
          可订9月22日
        </div>
        <div class="tags">
          <span>无需换票</span>
          <span>条件退</span>
          <span class="red">赠券￥1.0</span>
        </div>
      </div>
      <div class="buy">
        <div class="price">￥<span class="big">99</span></div>
        <router-link to="/" class="buy-btn">预订</router-link>
      </div>
    </div>
    <div class="item">
      <div class="infos">
        <div class="title">北京欢乐谷夜场票(9.17-9.21)</div>
        <div class="time">
          <img class="ticket-tagicon" src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png">
          可订9月22日
        </div>
        <div class="tags">
          <span>无需换票</span>
          <span>条件退</span>
        </div>
      </div>
      <div class="buy">
        <div class="price">￥<span class="big">59.9</span></div>
        <router-link to="/" class="buy-btn">预订</router-link>
      </div>
    </div>
    <div class="item">
      <div class="infos">
        <div class="title">北京欢乐谷成人票(下单三小时后生效)</div>
        <div class="time">
          <img class="ticket-tagicon" src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png">
          可订9月22日
        </div>
        <div class="tags">
          <span>可明日预订</span>
        </div>
      </div>
      <div class="buy">
        <div class="price">￥<span class="big">255.4</span></div>
        <router-link to="/" class="buy-btn">预订</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailRecommend'
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .d-recommend
    background-color #fff
    .header-title
      line-height $topHeigth
      padding-left .2rem
      font-size .32rem
      color #333
      i
        display inline-block
        vertical-align middle
        margin-bottom 4px
        width .36rem
        height .36rem
        line-height .36rem
        border-radius .36rem
        text-align center
        font-size .24rem
        background-color #ff8698
        color #fff
    .item
      display flex
      align-items center
      padding .2rem
      .infos
        flex 1
        .title
          line-height .52rem
          font-size .30rem
          color #666
        .time
          color #666
          margin-bottom .15rem
          font-size .24rem
          .ticket-tagicon
            width .2rem
        .tags
          font-size .24rem
          color #00afc7
          span
            margin-right .1rem
            &.red
              color #f55
      .buy
        width 1.6rem
        text-align center
        .price
          color $orange
          .big
            font-size .40rem
        .buy-btn
          display block
          line-height .6rem
          width 100%
          border-radius 4px
          background-image $orangeLinear
          color #fff
</style>
