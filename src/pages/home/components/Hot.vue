<template>
  <div class="hot">
    <div class="hot-header">
     <div class="hot-title">
      <img src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png">本周热门榜单
     </div>
     <div class="hot-more">
       全部榜单<span class="iconfont more">&#xe6dd;</span>
     </div>
    </div>
    <div class="hot-content">
      <div class="content-item" v-for="item of imgList" :key="item.id">
       <div class="item-img">
        <img class="content-img" :src="item.imgUrl">
       </div>
       <div class="item-title">{{item.imgTitle}}</div>
       <div class="item-price">
         ￥<span>{{item.imgPrice}}</span>起
       </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHot',
  data () {
    return {
      imgList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/6f/6f885ea8b30c67bca3.water.jpg_150x150_4abd4a25.jpg',
        imgTitle: '世界之窗',
        imgPrice: '39.9'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/17/176c2114bb8ae255a3.water.png_150x150_4e35377d.png',
        imgTitle: '深圳玛雅水公园',
        imgPrice: '69'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/17/176c2114bb8ae255a3.water.png_150x150_4e35377d.png',
        imgTitle: '深圳欢乐谷',
        imgPrice: '69'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_150x150_e7dd0cb5.jpg',
        imgTitle: '深圳野生动物园',
        imgPrice: '230'
      }, {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1611/97/97dbde6eccdfef72a3.water.jpg_150x150_47f5d64e.jpg',
        imgTitle: '东部华侨城',
        imgPrice: '164.01'
      }, {
        id: '006',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1702/9b/9b45082b3e38b2fda3.water.jpg_150x150_eac2bd99.jpg',
        imgTitle: '锦绣中华民俗村',
        imgPrice: '45'
      }, {
        id: '007',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/23/20f7be15157e2341055c05d40a5b57b9.jpg_150x150_fec30fa0.jpg',
        imgTitle: '深圳小梅沙海洋世界',
        imgPrice: '69.9'
      }, {
        id: '008',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/23/20f7be15157e2341055c05d40a5b57b9.jpg_150x150_fec30fa0.jpg',
        imgTitle: '东部华侨城大侠谷',
        imgPrice: '178'
      }, {
        id: '009',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201307/18/f25ac054eec3804dc8d65eac.jpg_150x150_d614b85b.jpg',
        imgTitle: '海洋奇梦馆',
        imgPrice: '50'
      }, {
        id: '010',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1608/6d/6d3c093626e8ceaca3.water.jpg_150x150_c5cc53c2.jpg',
        imgTitle: '华侨城',
        imgPrice: '39.9'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~style/ellipsis.styl'
  .hot-content
    white-space: nowrap
    overflow-x: scroll
    padding: 0 .24rem
    .content-item
      display: inline-block
      width: 2rem
      white-space: nowrap
      padding: .06rem 0 .2rem
      text-align: center
      font-size: .24rem
      &:not(:first-child)
        margin-left: .12rem
      .item-title
        margin-top: .12rem
        line-height: .32rem
        ellipsis()
      .item-price
        line-height: .36rem
        font-size: .24rem
        span
          color: #ff8300
          font-size: .28rem
      .item-img
        width: 2rem
        height: 0
        padding-bottom: 100%
        overflow:hidden
        img
          width:100%
  .hot-header
    display: flex
    justify-content: space-between
    padding: .24rem .32rem .26rem .2rem
    .hot-title
      font-size:.32rem
      img
        width:.3rem
        height:.3rem
        margin-top:-.1rem
    .hot-more
      font-size: .28rem
      display: flex
      align-items: center
</style>
