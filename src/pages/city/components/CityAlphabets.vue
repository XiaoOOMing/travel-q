<template>
  <div class="c-alphapets">
    <div class="title">字母排序</div>
    <div class="li-wrapper">
      <div class="li-item" v-for="item of city_alphabets" :key="item.id">{{ item.title }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabets',
  data () {
    return {
      city_alphabets: [
        {
          'id': 0,
          'title': 'A'
        },
        {
          'id': 1,
          'title': 'B'
        },
        {
          'id': 2,
          'title': 'C'
        },
        {
          'id': 3,
          'title': 'D'
        },
        {
          'id': 4,
          'title': 'E'
        },
        {
          'id': 5,
          'title': 'F'
        },
        {
          'id': 6,
          'title': 'G'
        },
        {
          'id': 7,
          'title': 'H'
        },
        {
          'id': 8,
          'title': 'J'
        },
        {
          'id': 9,
          'title': 'K'
        },
        {
          'id': 10,
          'title': 'L'
        },
        {
          'id': 11,
          'title': 'M'
        },
        {
          'id': 12,
          'title': 'N'
        },
        {
          'id': 13,
          'title': 'P'
        },
        {
          'id': 14,
          'title': 'Q'
        },
        {
          'id': 15,
          'title': 'R'
        },
        {
          'id': 16,
          'title': 'S'
        },
        {
          'id': 17,
          'title': 'T'
        },
        {
          'id': 18,
          'title': 'W'
        },
        {
          'id': 19,
          'title': 'X'
        },
        {
          'id': 20,
          'title': 'Y'
        },
        {
          'id': 21,
          'title': 'Z'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .c-alphapets
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
      padding .2rem 0
      .li-item
        color $gray
        width calc(100% / 6)
        text-align center
        line-height .9rem
</style>
