<template>
 <div class="wrap border-bottom">
 <swiper class="icons" :options="swiperOption">
   <swiper-slide v-for="(page,index) of pages" :key="index">
   <div class="icon" v-for="item of page" :key="item.id">
     <div class="icon-img"><img :src="item.imgUrl"></div>
     <div class="icon-text">{{item.imgTitle}}</div>
   </div>
   </swiper-slide>
   <div class="swiper-pagination" slot="pagination"></div>
 </swiper>
 <div class="onsale border-top">
   <div class="onsale-li border-right">定位失败</div>
   <div class="onsale-li">五折泡温泉</div>
 </div>
 </div>
</template>

<script>
export default {
  name: 'HomeIcon',
  data () {
    return {
      swiperOption: {
        loop: true,
        autoplay: false,
        pagination: '.swiper-pagination'
      },
      imgList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        imgTitle: '景点门票'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
        imgTitle: '游乐场'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
        imgTitle: '水上乐园'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
        imgTitle: '城市观光'
      }, {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        imgTitle: '一日游'
      }, {
        id: '006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        imgTitle: '动植物园'
      }, {
        id: '007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/27/dac2bcf9added702.png',
        imgTitle: '海滨海岛'
      }, {
        id: '008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
        imgTitle: '东部华侨城'
      }, {
        id: '009',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        imgTitle: '海洋馆'
      }, {
        id: '010',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',
        imgTitle: '全部玩乐'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.imgList.forEach(function (value, index) {
        const i = Math.floor(index / 8)
        if (!pages[i]) {
          pages[i] = []
        }
        pages[i].push(value)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  .border-top
    &:before
      border-color: #e0e0e0
.wrap >>> .swiper-pagination-bullet
    width: 6px
    height: 6px
  .onsale
    display: flex
    .onsale-li
      flex: 1
      line-height: .98rem
      height: .98rem
      font-size: .28rem
      text-align: center
  .icons
    overflow:hidden
    height:3.7rem
    padding-top:.1rem
    background:#fff
    .icon
      text-align:center
      float:left
      height:1.5rem
      width:25%
      padding-top:.1rem
      .icon-img
        width:1.1rem
        height:1.1rem
        display:inline-block
        img
          width:1.1rem
          height:1.1rem
      .icon-text
        margin-top:.1rem
        font-size:.28rem
        color:#212121
</style>
