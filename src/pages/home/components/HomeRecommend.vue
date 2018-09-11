<template>
    <div class="home-recommend">
      <div class="title-info">
        <div class="title">
          <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="本周热门榜单">
          猜你喜欢
        </div>
      </div>
      <div class="list-wrapper">
        <div class="item border-bottom" v-for="recommend of recommendList" :key="recommend.id">
          <div class="p-image-wrapper">
            <img :src="recommend.imgUrl" class="p-image">
          </div>
          <div class="p-info">
            <div class="p-title">
              {{ recommend.title }}
            </div>
            <div class="p-start-wrapper">
              <home-start :start="recommend.start"></home-start>
              <span>{{ recommend.comments }}条评论</span>
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
      </div>
      <div class="more">查看所有产品</div>
    </div>
</template>

<script>
import HomeStart from '@/common/start/CommonStart'

export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          'id': '0001',
          'title': '北京欢乐谷',
          'imgUrl': 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
          'comments': 2016487,
          'price': 59.9,
          'address': '东城区',
          'start': '5',
          'info': '👍小伙伴们都收藏了，去看看吧~'
        },
        {
          'id': '0002',
          'title': '故宫',
          'imgUrl': 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
          'comments': 287874,
          'price': 20,
          'address': '东城区',
          'start': '5',
          'info': '北京本月收藏Top5╰(￣▽￣)╭'
        },
        {
          'id': '0003',
          'title': '北京野生动物园',
          'imgUrl': 'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
          'comments': 13214,
          'price': 70,
          'address': '密云县',
          'start': '4',
          'info': ''
        },
        {
          'id': '0004',
          'title': '古北水镇',
          'imgUrl': 'http://img1.qunarzz.com/sight/p0/1804/c8/c88bb5e69c9a9c5ea3.img.jpg_200x200_740720ff.jpg',
          'comments': 7504,
          'price': 150,
          'address': '密云县',
          'start': '5',
          'info': '走进那个画中的小镇'
        }
      ]
    }
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
