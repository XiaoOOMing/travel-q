<template>
  <div class="city">
    <city-header></city-header>
    <city-hot-city></city-hot-city>
    <city-alphabets></city-alphabets>
    <city-list></city-list>
  </div>
</template>

<script>
import CityHeader from './components/CityHeader'
import CityHotCity from './components/CityHotCity'
import CityAlphabets from './components/CityAlphabets'
import CityList from './components/CityList'

export default {
  name: 'City',
  components: {
    CityHeader,
    CityHotCity,
    CityAlphabets,
    CityList
  }
}
</script>

<style scoped>

</style>
