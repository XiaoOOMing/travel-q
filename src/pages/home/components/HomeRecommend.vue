<template>
    <div class="home-recommend">
      <div class="title-info">
        <div class="title">
          <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="本周热门榜单">
          猜你喜欢
        </div>
      </div>
      <div class="list-wrapper">
        <router-link :to="'/detail?id=' + recommend.id" v-for="recommend of recommendLists" :key="recommend.id">
          <div class="item border-bottom">
            <div class="p-image-wrapper">
              <img :src="recommend.imgUrl" class="p-image">
            </div>
            <div class="p-info">
              <div class="p-title">
                {{ recommend.title }}
              </div>
              <div class="p-start-wrapper">
                <home-start :start="recommend.score"></home-start>
                <span>{{ recommend.comment }}条评论</span>
              </div>
              <div class="p-price-wrapper">
              <span class="p-price">
                <span class="orange">￥<span class="price">{{ recommend.price }}</span></span>
                起
              </span>
                <span class="address">{{ recommend.address }}</span>
              </div>
              <div v-if="recommend.info !== ''" class="hot-info">{{ recommend.info }}</div>
            </div>
          </div>
        </router-link>
      </div>
      <div class="more">查看所有产品</div>
    </div>
</template>

<script>
import HomeStart from '@/common/start/CommonStart'

export default {
  name: 'HomeRecommend',
  props: {
    recommendLists: Array
  },
  components: {
    HomeStart
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .home-recommend
    background #fff
    margin-top $marginTop
  .title-info
    display flex
    justify-content space-between
    align-items center
    height .44rem
    padding .24rem .2rem
    .title
      font-size .32rem
      .title-img
        width .3rem
        height .3rem
  .list-wrapper
    padding 0 .2rem
    .item
      padding .2rem 0
      display flex
      align-items top
      .p-image-wrapper
        width 2rem
        height 2rem
        .p-image
          width 100%
          height 100%
      .p-info
        flex 1
        padding-left .2rem
        .p-title
          color #444
          padding .2rem 0
          font-size 0.32rem
          margin-bottom .15rem
        .p-start-wrapper
          display flex
          align-items center
          padding-bottom .2rem
          font-size .24rem
          color $gray
          span
            margin-left .2rem
        .p-price-wrapper
          color $gray
          display flex
          justify-content space-between
          align-items center
          .p-price
            font-size .24rem
            .orange
              color $orange
            .price
              font-size .36rem
              font-weight bold
      .hot-info
        display inline-block
        color #f55
        background #fff9f9
        font-size .24rem
        margin-top .48rem
  .more
    text-align center
    line-height .8rem
    color $bgColor
</style>
