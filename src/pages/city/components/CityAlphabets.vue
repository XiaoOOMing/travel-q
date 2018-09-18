<template>
  <div class="c-alphapets">
    <div class="title">字母排序</div>
    <div class="li-wrapper">
      <a :href="'#anchor-' + item.title" class="li-item" v-for="item of city_alphabets" :key="item.id">{{ item.title }}</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabets',
  props: {
    city_alphabets: Array
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
