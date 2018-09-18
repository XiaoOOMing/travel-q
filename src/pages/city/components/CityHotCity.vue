<template>
  <div class="c-hot-city">
    <div class="title">热门城市</div>
    <div class="li-wrapper">
      <div class="lines"></div>
      <div class="li-item"
           v-for="item of hot_cities"
           :key="item.id" @click="handleChangeCity(item.title)">{{ item.title }}</div>
    </div>
  </div>
</template>

<script>
import {mapMutations} from 'vuex'

export default {
  name: 'CityHotCity',
  props: {
    hot_cities: Array
  },
  methods: {
    handleChangeCity (name) {
      this.changeCity(name)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .c-hot-city
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
        width calc(100% / 3)
        height 100%
        border-left 1px solid #eee
        border-right 1px solid #eee
        top 0
        left calc(100% / 3)
        z-index 1
      .li-item
        position relative
        z-index 9
        width calc(100% / 3)
        text-align center
        line-height $topHeigth
        border-bottom 1px solid #eee
</style>
