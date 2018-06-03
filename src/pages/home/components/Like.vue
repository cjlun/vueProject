<template>
  <div class="like">
    <div class="like-title">
      <img src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png"> 猜你喜欢
    </div>
    <ul class="like-items">
      <li class="like-item border-bottom" v-for="item of imgList" :key="item.id">
        <div class="like-item-img">
          <img :src="item.imgUrl">
        </div>
        <div class="like-item-text">
          <div class="item-title">{{item.imgTitle}}</div>
          <div class="item-grade"><span class="star">★★★★★</span>&nbsp;&nbsp;&nbsp;{{item.imgReview}}条评论</div>
          <div class="item-priceArea">
           <div>          
            <span class="item-price">￥<em>{{item.imgPrice}}</em></span>起
           </div>
           <div>{{item.imgAddress}}</div>
          </div>
          <div class="item-feature" v-show="item.imgFeature">{{item.imgFeature}}</div>
        </div>
      </li>
    </ul>
    <div class="like-footer">
      查看所有产品
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeLike',
  data () {
    return {
      imgList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/17/176c2114bb8ae255a3.water.png_200x200_a1b6cfdf.png',
        imgTitle: '深圳欢乐谷',
        imgGrade: '',
        imgReview: '18841',
        imgPrice: '69',
        imgAddress: '南山区',
        imgFeature: '狂欢无罪，够胆你就来'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/6f/6f885ea8b30c67bca3.water.jpg_200x200_21b03a9c.jpg',
        imgTitle: '世界之窗',
        imgGrade: '',
        imgReview: '23753',
        imgPrice: '39.9',
        imgAddress: '华侨城',
        imgFeature: '深圳本月收藏Top5╰(￣▽￣)╭'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
        imgTitle: '深圳野生动物园',
        imgGrade: '',
        imgReview: '11238',
        imgPrice: '230',
        imgAddress: '南山区',
        imgFeature: '近期小伙伴们收藏最！多！的景点😊'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1611/97/97dbde6eccdfef72a3.water.jpg_200x200_e0efe6da.jpg',
        imgTitle: '东部华侨城',
        imgGrade: '',
        imgReview: '15076',
        imgPrice: '164.01',
        imgAddress: '盐田区',
        imgFeature: ''
      }, {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201307/18/f25ac054eec3804dc8d65eac.jpg_200x200_a008b6ca.jpg',
        imgTitle: '海洋奇梦馆',
        imgGrade: '',
        imgReview: '2961',
        imgPrice: '50',
        imgAddress: '欢乐海岸',
        imgFeature: '帅的人都去过了😎，你还等什么~'
      }, {
        id: '006',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/17/176c2114bb8ae255a3.water.png_200x200_a1b6cfdf.png',
        imgTitle: '深圳玛雅水公园',
        imgGrade: '',
        imgReview: '425',
        imgPrice: '69',
        imgAddress: '深圳欢乐...',
        imgFeature: ''
      }, {
        id: '007',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/23/20f7be15157e2341055c05d40a5b57b9.jpg_200x200_08c98b9d.jpg',
        imgTitle: '东部华侨城大侠谷',
        imgGrade: '',
        imgReview: '4524',
        imgPrice: '178',
        imgAddress: '东部华侨...',
        imgFeature: ''
      }, {
        id: '008',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/64/34362835b4a219af8b36803d31a6380f.water.jpg_200x200_bc5c0452.jpg',
        imgTitle: '深圳小梅沙海洋世界',
        imgGrade: '',
        imgReview: '5233条评论',
        imgPrice: '69.9',
        imgAddress: '小梅沙',
        imgFeature: '一天穿越四大洋'
      }, {
        id: '009',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/30/a9edfcb4fe0e119da480d30d22ade127.jpg_200x200_6af441cf.jpg',
        imgTitle: '地王大厦',
        imgGrade: '',
        imgReview: '2846',
        imgPrice: '70',
        imgAddress: '罗湖区',
        imgFeature: ''
      }, {
        id: '010',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/e4/a3f526c57e0115798af52929d294ddd6.water.jpg_200x200_c6bc3621.jpg',
        imgTitle: '东部华侨城茶溪谷',
        imgGrade: '',
        imgReview: '4595',
        imgPrice: '164.01',
        imgAddress: '东部华侨...',
        imgFeature: ''
      }, {
        id: '011',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/ab/ab4fccbc392da994a3.water.jpg_200x200_0b4dfdea.jpg',
        imgTitle: '观澜山水田园水上乐园',
        imgGrade: '',
        imgReview: '581',
        imgPrice: '75',
        imgAddress: '观澜山水...',
        imgFeature: '提供适合不同年龄层次游客的游乐项目'
      }, {
        id: '012',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201307/15/7eab0785f2aa37e8c8d65eac.jpg_200x200_ca7ce0e0.jpg',
        imgTitle: '大梅沙',
        imgGrade: '',
        imgReview: '2471',
        imgPrice: '164.01',
        imgAddress: '盐田区',
        imgFeature: ''
      }, {
        id: '013',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1504/25/2567e9dc989e2eb6.water.jpg_200x200_caea32c8.jpg',
        imgTitle: '金色海岸游艇',
        imgGrade: '',
        imgReview: '648',
        imgPrice: '90',
        imgAddress: '盐田区',
        imgFeature: ''     
      }, {
        id: '014',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201303/04/3dc3e87356026a63c8d65eac.jpg_200x200_1de448b6.jpg',
        imgTitle: '阿尔卑斯山滑雪场',
        imgGrade: '',
        imgReview: '810',
        imgPrice: '45',
        imgAddress: '世界之窗',
        imgFeature: ''
      }, {
        id: '015',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1702/9b/9b45082b3e38b2fda3.water.jpg_200x200_785628c9.jpg',
        imgTitle: '锦绣中华民俗村',
        imgGrade: '',
        imgReview: '11485',
        imgPrice: '45',
        imgAddress: '华侨城',
        imgFeature: ''
      }, {
        id: '016',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/e8/2c6ac21e08d919610ee5e7b8b95be052.water.jpg_200x200_704f0dda.jpg',
        imgTitle: '小梅沙',
        imgGrade: '',
        imgReview: '3078',
        imgPrice: '48',
        imgAddress: '盐田区',
        imgFeature: ''
      }, {
        id: '017',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1504/4d/4db8a74c30f97af7.water.jpg_200x200_d65c7a5e.jpg',
        imgTitle: '青青世界',
        imgGrade: '',
        imgReview: '2022',
        imgPrice: '40',
        imgAddress: '南山区',
        imgFeature: ''
      }, {
        id: '018',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/5a/5a86bea723aca30ca3.water.png_200x200_541e78d2.png',
        imgTitle: '欢乐海岸',
        imgGrade: '',
        imgReview: '3018',
        imgPrice: '50',
        imgAddress: '南山区',
        imgFeature: '屌丝或是高富帅，都有你的栖息之地'
      }, {
        id: '019',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1702/5e/5ef114ef3288db33a3.water.jpg_200x200_f662aeb6.jpg',
        imgTitle: '刘老根拿来一壶嗨',
        imgGrade: '',
        imgReview: '285',
        imgPrice: '38',
        imgAddress: '福田区',
        imgFeature: ''
      }, {
        id: '020',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1608/6d/6d3c093626e8ceaca3.water.jpg_200x200_ffa505fa.jpg',
        imgTitle: '华侨城',
        imgGrade: '',
        imgReview: '18430',
        imgPrice: '39.9',
        imgAddress: '南山区',
        imgFeature: ''
      }, {
        id: '021',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1701/39/39982ad22a210ecca3.water.jpg_200x200_950c135d.jpg',
        imgTitle: '流星谷欢乐世界',
        imgGrade: '',
        imgReview: '159',
        imgPrice: '39',
        imgAddress: '宝安区',
        imgFeature: '提供一个优闲、生态、浪漫的极佳去处'
      }, {
        id: '022',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1510/d0/d0610302e0ae770890.water.jpg_200x200_2ce068f1.jpg',
        imgTitle: '东部华侨城茵特拉根温泉',
        imgGrade: '',
        imgReview: '1672',
        imgPrice: '76.1',
        imgAddress: '盐田区',
        imgFeature: '帅的人都去过了😎，你还等什么~'
      }, {
        id: '023',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/96/96f47768e63ffdbe90.water.jpg_200x200_27a76824.jpg',
        imgTitle: '海上田园',
        imgGrade: '',
        imgReview: '1632',
        imgPrice: '55',
        imgAddress: '宝安区',
        imgFeature: ''
      }, {
        id: '024',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1611/de/ded011f10ed4bf16a3.water.jpg_200x200_103c1a5c.jpg',
        imgTitle: '西冲情人岛',
        imgGrade: '',
        imgReview: '186',
        imgPrice: '3.6',
        imgAddress: '深圳',
        imgFeature: '深圳的世外桃源'
      }, {
        id: '025',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/30/258359fbfa587e26a207cee0ffe39211.jpg_200x200_26567159.jpg',
        imgTitle: '观澜山水田园旅游文化园',
        imgGrade: '',
        imgReview: '1096',
        imgPrice: '75',
        imgAddress: '龙华新区',
        imgFeature: ''
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .like-title
    padding: .24rem 0 .26rem .2rem
    height: .44rem
    line-height: .44rem
    font-size: .32rem
    img
      width: .3rem
      height: .3rem
      vertical-align: top
  .like-items
    margin-left: .24rem
    .like-item
      padding: .2rem 0
      display: flex
      .like-item-img
        width: 2rem
        height: 2rem
        overflow: hidden
        img
          width:100%
      .like-item-text
        flex: 1
        padding-left: .22rem
        .item-title
          font-size: .32rem
          margin-top: .26rem
          height: .44rem
          line-height: .44rem
        .item-grade
          margin-top: .14rem
          font-size: .24rem
          line-height: .34rem
          height: .34rem
          .star
            color: #ffb436
            font-size: .28rem
        .item-priceArea
          display: flex
          justify-content: space-between
          margin-top: .22rem
          line-height: .4rem
          font-size: .24rem
          padding-right: .24rem
          .item-price
            color: #ff8300
            em
              font-size: .4rem
        .item-feature
          margin-top: .48rem
          margin-right: .24rem
          color: #f55
  .like-footer
    color: #00afc7
    padding: .2rem 0
    font-size: .28rem
    line-height: .4rem
    text-align: center
</style>
