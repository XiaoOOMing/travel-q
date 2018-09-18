<template>
  <div class="detail">
    <detail-header></detail-header>
    <detail-banner></detail-banner>
    <div style="height: 30rem"></div>
  </div>
</template>

<script>
import DetailHeader from './components/DetailHeader'
import DetailBanner from './components/DetailBanner'
export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailBanner
  }
}
</script>

<style scoped>

</style>
