<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-adv></home-adv>
    <home-rank></home-rank>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/HomeIcons'
import HomeAdv from './components/HomeAdv'
import HomeRank from './components/HomeRank'
import HomeRecommend from './components/HomeRecommend'
import HomeWeekend from './components/HomeWeekend'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeAdv,
    HomeRank,
    HomeRecommend,
    HomeWeekend
  }
}
</script>

<style scoped>

</style>
