<template>
 <div class="wrap">
 <swiper :options="swiperOption" v-if="swiper.length">
   <swiper-slide v-for="(item,index) of swiper" :key="index">
     <div class="img"><img :src="item" /></div>
   </swiper-slide>
   <div class="swiper-pagination"  slot="pagination"></div>
 </swiper>
 </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: ['swiper'],
  data () {
    return {
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
.wrap
  height: 0
  overflow: hidden
  padding-bottom: 26.67%
  img
    width:100%
</style>
