<template>
  <div class="home-icons">
    <swiper :options="swiperOption" class="swiper">
      <swiper-slide v-for="(iconPage, index) of icons" :key="index">
        <div class="icons-container">
          <div class="icons-item" v-for="icon of iconPage" :key="icon.id">
            <img :src="icon.imgUrl" class="icon-image">
            <div class="icon-title">
              {{ icon.title }}
            </div>
          </div>
        </div>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    <div class="t-wrapper border-top">
      <div class="t-item border-right">
        <i class="iconfont">&#xe611;</i>
        定位失败
      </div>
      <div class="t-item">
        <i class="iconfont">&#xe642;</i>
        玩水季
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      },
      iconLists: [
        {
          id: '0001',
          title: '景点门票',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
        },
        {
          id: '0002',
          title: '北京必游',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png'
        },
        {
          id: '0003',
          title: '夏日玩水',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png'
        },
        {
          id: '0004',
          title: '文化古迹',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png'
        },
        {
          id: '0005',
          title: '动植物园',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png'
        },
        {
          id: '0006',
          title: '故宫',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png'
        },
        {
          id: '0007',
          title: '一日游',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png'
        },
        {
          id: '0008',
          title: '国家宝藏',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/8d/747c9a29b8dba402.png'
        },
        {
          id: '0009',
          title: '游乐场',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png'
        },
        {
          id: '0010',
          title: '全部玩乐',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png'
        }
      ]
    }
  },
  computed: {
    icons () {
      let iconNum = 8
      let res = []
      this.iconLists.forEach((item, index) => {
        let arrIndex = Math.floor(index / iconNum)
        if (!res[arrIndex]) {
          res[arrIndex] = []
        }
        res[arrIndex].push(item)
      })
      return res
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .home-icons >>> .swiper-pagination-bullets
    bottom .1rem
    padding-left .12rem
  .home-icons >>> .swiper-pagination-bullet
    width .12rem
    height .12rem
    background rgba(144,144,144,0.8)
    margin 0 .08rem
    opacity 1
  .home-icons
    background #fff
  .swiper >>> .swiper-pagination-bullet-active
    background $bgColor
    opacity 1
  .icons-container
    display flex
    justify-content flex-start
    flex-wrap wrap
    padding-top .1rem
    padding-bottom .5rem
    .icons-item
      padding-top .1rem
      width 25%
      .icon-image
        display block
        width 1.1rem
        height 1.1rem
        margin 0 auto
      .icon-title
        text-align center
        font-size .28rem
        margin-top .08rem
  .t-wrapper
    display flex
    .t-item
      width 50%
      text-align center
      line-height .98rem
</style>
