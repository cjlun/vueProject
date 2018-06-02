<template>
 <swiper :options="swiperOption">
   <swiper-slide v-for="(item,index) of imgList" :key="index">
     <div class="img"><img :src="item" /></div>
   </swiper-slide>
   <div class="swiper-pagination"  slot="pagination"></div>
 </swiper>

</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      imgList: ['http://img1.qunarzz.com/piao/fusion/1805/77/f63bd04dd5319602.jpg_750x200_6ba8e0ca.jpg', 'http://img1.qunarzz.com/piao/fusion/1805/77/f63bd04dd5319602.jpg_750x200_6ba8e0ca.jpg'],
      swiperOption: {
        loop: true,
        autoplay: false,
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  >>> .swiper-pagination-bullet
    width: 6px
    height: 6px
  .img
    height: 0
    overflow: hidden
    padding-bottom: 26.67%
    img
      width:100%
</style>
