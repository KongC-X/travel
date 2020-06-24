<template>
  <div><div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper"><img class="item-img" :src="item.imgUrl"></div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
      </div>
    </li>
  </ul></div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1905/44/44c6db1f35f281f6a3.water.jpg_710x360_bad489bd.jpg',
        title: '南浔古镇',
        desc: '水乡古镇九十九，不如南浔走一走'
      },
      {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1905/44/44c6db1f35f281f6a3.water.jpg_710x360_bad489bd.jpg',
        title: '西塘古镇',
        desc: '水墨西塘让你感受古镇千年的诗情画意'
      },
      {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1905/44/44c6db1f35f281f6a3.water.jpg_710x360_bad489bd.jpg',
        title: '普陀山风景区',
        desc: '人间清净地 | 朝圣看日出'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 50%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
       line-height .4rem
       color #ccc
       ellipsis()
</style>
