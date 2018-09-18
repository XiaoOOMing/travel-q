<template>
  <swiper :options="swiperOption" class="swiper" v-if="showSwiper">
    <!-- slides -->
    <swiper-slide v-for="item of swipers" :key="item.id" class="swiper-container">
      <img :src="item.imgUrl" class="swiper-image">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    swipers: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 5000
      }
    }
  },
  computed: {
    showSwiper () {
      return this.swipers.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .swiper >>> .swiper-pagination-bullets
    bottom .1rem
  .swiper >>> .swiper-pagination-bullet
    width .12rem
    height .12rem
    background #fff
    opacity .4
    margin 0 .08rem
  .swiper >>> .swiper-pagination-bullet-active
    background #fff
    opacity 1
  .swiper-container
    width 100%
    height 0
    padding-bottom 26.7%
    overflow hidden
    .swiper-image
      width 100%
</style>
