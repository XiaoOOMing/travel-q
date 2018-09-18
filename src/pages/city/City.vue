<template>
  <div class="city">
    <city-header></city-header>
    <city-hot-city :hot_cities="hot_cities"></city-hot-city>
    <city-alphabets :city_alphabets="city_alphabets"></city-alphabets>
    <city-list :cityList="cityList"></city-list>
  </div>
</template>

<script>
import CityHeader from './components/CityHeader'
import CityHotCity from './components/CityHotCity'
import CityAlphabets from './components/CityAlphabets'
import CityList from './components/CityList'
import axios from 'axios'

export default {
  name: 'City',
  data () {
    return {
      cityList: [],
      city_alphabets: [],
      hot_cities: []
    }
  },
  components: {
    CityHeader,
    CityHotCity,
    CityAlphabets,
    CityList
  },
  methods: {
    getCityInfo () {
      axios.get('/static/api/city.json')
        .then(this.getCityInfoSuccess)
    },
    getCityInfoSuccess (res) {
      console.log(res)
      let data = res.data
      this.cityList = data.cityList
      this.city_alphabets = data.city_alphabets
      this.hot_cities = data.hot_cities
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style scoped>

</style>
