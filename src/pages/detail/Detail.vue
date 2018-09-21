<template>
  <div class="detail">
    <detail-header></detail-header>
    <detail-banner></detail-banner>
    <detail-info></detail-info>
    <detail-recommend></detail-recommend>
    <detai-ticket></detai-ticket>
    <div style="height: 30rem"></div>
  </div>
</template>

<script>
import DetailHeader from './components/DetailHeader'
import DetailBanner from './components/DetailBanner'
import DetailInfo from './components/DetailInfo'
import DetailRecommend from './components/DetailRecommend'
import DetaiTicket from './components/DetaiTicket'
export default {
  name: 'Detail',
  components: {
    DetailHeader,
    DetailBanner,
    DetailInfo,
    DetailRecommend,
    DetaiTicket
  }
}
</script>

<style scoped>

</style>
