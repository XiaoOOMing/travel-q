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
  data () {
    return {
      hot_cities: [
        {
          'id': 0,
          'title': '北京'
        },
        {
          'id': 1,
          'title': '上海'
        },
        {
          'id': 2,
          'title': '三亚'
        },
        {
          'id': 3,
          'title': '香港'
        },
        {
          'id': 4,
          'title': '杭州'
        },
        {
          'id': 5,
          'title': '广州'
        },
        {
          'id': 6,
          'title': '成都'
        },
        {
          'id': 7,
          'title': '深圳'
        },
        {
          'id': 8,
          'title': '苏州'
        },
        {
          'id': 9,
          'title': '桂林'
        },
        {
          'id': 10,
          'title': '西安'
        },
        {
          'id': 11,
          'title': '厦门'
        }
      ]
    }
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
