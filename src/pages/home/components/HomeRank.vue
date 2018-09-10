<template>
  <div class="home-rank">
    <div class="title-info">
      <div class="title">
        <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="本周热门榜单">
        本周热门榜单
      </div>
      <div class="more">
        全部榜单
        <i class="iconfont">&#xe624;</i>
      </div>
    </div>
    <div class="ranks">
      <ul class="rank-container">
        <li class="rank-item" v-for="(item, index) of rankList" :key="item.id">
          <img :src="item.imgUrl" class="rank-image">
          <div class="title">{{ item.title }}</div>
          <div class="title">
            <span class="orange">￥{{ item.min_price }}</span>起</div>
          <div class="rank-number" v-html="medal(index)"></div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeRank',
  data () {
    return {
      rankList: [
        {
          id: '0001',
          title: '故宫',
          min_price: 20,
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_150x150_06cb3e52.jpg'
        },
        {
          id: '0002',
          title: '八达岭长城',
          min_price: 40,
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_150x150_2dec3e78.jpg'
        },
        {
          id: '0003',
          title: '八达岭长城缆车',
          min_price: 160,
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201306/13/bdf22f69fab0ee4ec8d65eac.jpg_150x150_35b4b15f.jpg'
        },
        {
          id: '0004',
          title: '颐和园',
          min_price: 41,
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/d2/d274c92de14c93da.water.jpg_150x150_2747e538.jpg'
        },
        {
          id: '0005',
          title: '水立方',
          min_price: 14,
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_150x150_8a63d940.jpg'
        },
        {
          id: '0006',
          title: '圆明园',
          min_price: 9.8,
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/f5/f5f45e1a83537bcb.water.jpg_150x150_2a3c9117.jpg'
        }
      ]
    }
  },
  methods: {
    medal (index) {
      if (index === 0) {
        return '<img style="height: .4rem" src="http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png">'
      } else if (index === 1) {
        return ' <img style="height: .4rem" src="http://img1.qunarzz.com/piao/fusion/1710/2d/36d0c4adaebbbc02.png">'
      } else if (index === 2) {
        return '<img style="height: .4rem" src="http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png">'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .home-rank
    margin-top $marginTop
    background #fff
    padding-bottom .2rem
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
    .more
      font-size .24rem
      color #666
      .iconfont
        display inline-block
        transform rotate(-180deg)
        font-size .24rem
  .ranks
    width 100%
    overflow-y scroll
    .rank-container
      display flex
      flex-wrap nowrap
      padding 0 .24rem
      padding-top .1rem
      margin 0
      .rank-item
        list-style none
        margin-right .12rem
        position relative
        .rank-image
          width 2rem
          height 2rem
        .title
          margin-top .1rem
          color #333
          font-size .24rem
          text-align center
          .orange
            color $orange
        .rank-number
          position absolute
          top -.05rem
          left 0rem
</style>
