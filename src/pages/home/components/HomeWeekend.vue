<template>
  <div class="home-weekend">
    <div class="title">周末去哪儿</div>
    <div class="li-wrapper">
      <div class="li-item" v-for="item of weekendList" :key="item.id">
        <div class="image-wrapper">
          <img :src="item.imgUrl">
        </div>
        <div class="info-wrapper">
          <div class="title">{{ item.title }}</div>
          <div class="desc">{{ item.desc }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@css/variable.styl"
  .home-weekend
    & > .title
      line-height .8rem
      padding 0 .2rem
    .li-wrapper
      .li-item
        background #fff
        margin-bottom .1rem
        .image-wrapper
          img
            width 100%
        .info-wrapper
          padding .2rem
          .title
            margin-bottom .1rem
          .desc
            font-size .24rem
            color $gray
</style>
