<template>
  <div class="home-weekend">
    <div class="title">周末去哪儿</div>
    <div class="li-wrapper">
      <div class="li-item" v-for="item of weekList" :key="item.id">
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
  data () {
    return {
      weekList: [
        {
          id: '0001',
          title: '漂流勇进，烧烤露营',
          desc: '轻松水上漂，任我乐逍遥',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg'
        },
        {
          id: '0002',
          title: '北京清凉避暑胜地',
          desc: '到大自然中享受“天然空调”的清凉',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/53/02091f1ee43d0a.jpg_r_640x214_2e3256b1.jpg'
        },
        {
          id: '0003',
          title: '北京必游TOP10',
          desc: '来北京必去的景点非这些地方莫属',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg'
        },
        {
          id: '0004',
          title: '寻找北京的皇城范儿',
          desc: '数百年的宫廷庙宇，至今依旧威严霸气',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg'
        },
        {
          id: '0005',
          title: '学生最爱的博物馆',
          desc: '周末干嘛？北京很多博物馆已经免费开放啦',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ce/bc89bc2f0e33ea.jpg_r_640x214_3e408453.jpg'
        }
      ]
    }
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
