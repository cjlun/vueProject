<template>
  <div class="weekend">
    <div class="weekend-header">周末去哪儿</div>
    <div class="weekend-items">
      <div class="weekend-item" v-for="item of imgList" :key="item.id">
        <div class="weekend-item-img">
          <img class="image" :src="item.imgUrl">
        </div>
       <div class="weekend-item-text">
        <div class="weekend-item-name">{{item.imgTitle}}</div>
        <div class="weekend-item-desc">{{item.imgDesc}}</div>
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
      imgList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
        imgTitle: '深圳必游TOP10',
        imgDesc: '来到深圳，你需要来这里签到'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1602/88/bf120edeaea383.jpg_r_640x214_f8591f7b.jpg',
        imgTitle: '欢乐长隆',
        imgDesc: '世界欢乐汇聚长隆'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1507/d9/2ddc7652fdba16.jpg_r_640x214_5e62f1a3.jpg',
        imgTitle: '当地人游深圳',
        imgDesc: '当地人带你发现不一样的深圳'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/eb/e4b181a6957c36.jpg_r_640x214_4abbdbc0.jpg',
        imgTitle: '情侣好去处',
        imgDesc: '手牵手，一起走到老'
      }, {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/69/e899202f7abddf.jpg_r_640x214_81b6b528.jpg',
        imgTitle: '周末亲子游',
        imgDesc: '这个周末就开启美妙的亲子时光'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~style/ellipsis.styl'
  .weekend-header
    padding-left: .26rem
    line-height: .8rem
    height: .8rem
    color: #212121
    background: #f5f5f5
  .weekend-items
    .weekend-item-text
      padding: .14rem .2rem .2rem .2rem
      .weekend-item-name
        line-height: .48rem
        padding-right: 1.4rem
        ellipsis()
      .weekend-item-desc
        line-height: .42rem
        font-size: .24rem
        padding-right: 1.4rem
        ellipsis()
    .weekend-item-img
      height: 0
      padding-bottom: 37.4375%
      overflow: hidden
      .image
        width: 100%
</style>
