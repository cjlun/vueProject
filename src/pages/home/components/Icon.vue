<template>
 <div class="wrap border-bottom">
 <div class="wrap-swiper">
 <swiper class="icons" :options="swiperOption" v-if="icon.length">
   <swiper-slide v-for="(page,index) of pages" :key="index">
   <div class="icon" v-for="item of page" :key="item.id">
     <div class="icon-img"><img :src="item.imgUrl"></div>
     <div class="icon-text">{{item.imgTitle}}</div>
   </div>
   </swiper-slide>
   <div class="swiper-pagination" slot="pagination"></div>
 </swiper>
 </div>
 <div class="onsale border-top">
   <div class="onsale-li border-right">定位失败</div>
   <div class="onsale-li">五折泡温泉</div>
 </div>
 </div>
</template>

<script>
export default {
  name: 'HomeIcon',
  props: ['icon'],
  data () {
    return {
      swiperOption: {
        loop: true,
        autoplay: false,
        pagination: '.swiper-pagination'
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.icon.forEach(function (value, index) {
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
  .wrap-swiper
    height: 3.8rem
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
