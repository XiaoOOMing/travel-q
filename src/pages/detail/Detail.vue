<template>
  <div class="detail">
    <detail-header></detail-header>
    <detail-banner></detail-banner>
    <detail-info></detail-info>
    <div style="height: 30rem"></div>
  </div>
</template>

<script>
import DetailHeader from './components/DetailHeader'
import DetailBanner from './components/DetailBanner'
import DetailInfo from './components/DetailInfo'
export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailBanner,
    DetailInfo
  }
}
</script>

<style scoped>

</style>
