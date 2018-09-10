<template>
  <div class="start">
    <i class="iconfont" v-for="(item, index) of number" :key="index">&#xe8c2;</i>
  </div>
</template>

<script>
export default {
  name: 'CommonStart',
  props: {
    start: [Number, String]
  },
  computed: {
    number () {
      return Math.round(this.start)
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .start
    display flex
    align-items center
    width 1.2rem
    overflow hidden
    .iconfont
      color $yellow
      font-size .24rem
</style>
