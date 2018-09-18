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
  props: {
    iconLists: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      }
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
