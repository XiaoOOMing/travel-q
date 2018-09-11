<template>
  <div class="city">
    <city-header></city-header>
    <city-hot-city></city-hot-city>
    <city-alphabets></city-alphabets>
  </div>
</template>

<script>
import CityHeader from './components/CityHeader'
import CityHotCity from './components/CityHotCity'
import CityAlphabets from './components/CityAlphabets'

export default {
  name: 'City',
  components: {
    CityHeader,
    CityHotCity,
    CityAlphabets
  }
}
</script>

<style scoped>

</style>
