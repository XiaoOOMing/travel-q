<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper :swipers="swipers"></home-swiper>
    <home-icons :iconLists="iconLists"></home-icons>
    <home-adv></home-adv>
    <home-rank :hot_sale="hot_sale"></home-rank>
    <home-recommend :recommendLists="recommendLists"></home-recommend>
    <home-weekend :weekendList="weekendList"></home-weekend>
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
import axios from 'axios'

export default {
  name: 'Home',
  data () {
    return {
      swipers: [],
      iconLists: [],
      hot_sale: [],
      recommendLists: [],
      weekendList: []
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeAdv,
    HomeRank,
    HomeRecommend,
    HomeWeekend
  },
  methods: {
    getHomeInfo () {
      axios.get('/static/api/home.json')
        .then(this.getHomeInfoSuccess)
    },
    getHomeInfoSuccess (res) {
      let data = res.data
      this.swipers = data.swipers
      this.iconLists = data.iconList
      this.hot_sale = data.hot_sale
      this.recommendLists = data.recommendLists
      this.weekendList = data.weekendList
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style scoped>

</style>
