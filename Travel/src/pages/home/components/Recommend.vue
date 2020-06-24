<template>
  <div><div class="title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>
    </li>
  </ul></div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: '//img1.qunarzz.com/sight/p0/1601/1c/1cdfd6a29fd1813990.img.jpg_256x160_87ff1663.jpg',
        title: '南浔古镇',
        desc: '水乡古镇九十九，不如南浔走一走'
      },
      {
        id: '0002',
        imgUrl: '//img1.qunarzz.com/sight/p0/1607/21/2142167d4b1bfa84b4.water.jpg_256x160_ea65b4f7.jpg',
        title: '西塘古镇',
        desc: '水墨西塘让你感受古镇千年的诗情画意'
      },
      {
        id: '0003',
        imgUrl: '//img1.qunarzz.com/sight/p0/1603/8f/8fff2332dff679ec90.water.jpg_256x160_224237e3.jpg',
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
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .16rem
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #fff
</style>
