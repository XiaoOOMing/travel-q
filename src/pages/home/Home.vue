<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-adv></home-adv>
    <home-rank></home-rank>
    <home-recommend></home-recommend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/HomeIcons'
import HomeAdv from './components/HomeAdv'
import HomeRank from './components/HomeRank'
import HomeRecommend from './components/HomeRecommend'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeAdv,
    HomeRank,
    HomeRecommend
  }
}
</script>

<style scoped>

</style>
