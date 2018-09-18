<template>
  <div class="city-list">
    <div v-for="item of cityList" :key="item.id" :id="'anchor-' + item.alpha">
      <div class="title">{{ item.alpha }}</div>
      <div class="li-wrapper">
        <div class="lines"></div>
        <div class="lines-2"></div>
        <div class="li-item"
             v-for="(cityName,index) of item.cities"
             :key="index" @click="handleCity(cityName)">{{ cityName }}</div>
      </div>
    </div>
  </div>
</template>

<script>
import {mapMutations} from 'vuex'

export default {
  name: 'CityList',
  props: {
    cityList: Array
  },
  methods: {
    handleCity (name) {
      this.changeCity(name)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  @import "~@css/mixin.styl"
  .city-list
    .title
      font-size .24rem
      line-height $topHeigth
      padding 0 .2rem
    .li-wrapper
      position relative
      background #fff
      display flex
      flex-wrap wrap
      justify-content flex-start
      .lines
        position absolute
        z-index 1
        width 25%
        height 100%
        border-left 1px solid #eee
        border-right 1px solid #eee
        top 0
        left 25%
      .lines-2
        position absolute
        z-index: 1
        width .02rem
        height 100%
        border-left 1px solid #eee
        top 0
        left 75%
      .li-item
        position relative
        z-index: 9
        ellipse()
        width 25%
        text-align center
        line-height $topHeigth
        border-bottom 1px solid #eee
</style>
