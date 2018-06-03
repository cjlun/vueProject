<template>
  <div class="footer">
   <div>
    <div class="look">
      <span class="iconfont lookIcon">&#xe622;</span><em>票面价</em>是指通过景区指定窗口售卖的纸质门票上标注的价格
    </div>
    <div class="main-nav">
      <ul class="main-nav-items">
        <li class="main-nav-item">
          <div class="icon"></div>
          <span class="icon-text">机票</span>
        </li>
        <li class="main-nav-item">
          <div class="icon hotel"></div>
          <span class="icon-text">酒店</span>
        </li>
        <li class="main-nav-item">
          <div class="icon flat"></div>
          <span class="icon-text">公寓</span>
        </li>
        <li class="main-nav-item">
          <div class="more"><span class="iconfont">&#xe601;</span>更多</div>
        </li>
      </ul>
    </div>
    <div class="mySystem">
      <div class="mySystem-item">登录</div>
      <div class="mySystem-item">我的订单</div>
      <div class="mySystem-item">最近浏览</div>
      <div class="mySystem-item">关于我们</div>
    </div>
   </div>
   <div class="version">
     <div class="tab-version">
       <div class="tab-version-item">触屏版</div>
       <div class="tab-version-item">电脑版</div>
     </div>
     <div class="suggest">
       Qunar 京ICP备05021087<span>意见反馈</span>
     </div>
   </div>
  </div>
</template>

<script>
export default {
  name: 'HomeFooter'
}
</script>

<style lang="stylus" scoped>
.footer
  background: #f3f3f3
  .version
    text-align: center
    .suggest
      color: #9e9e9e
      padding: 10px
    .tab-version
      padding-top: 10px
      display:flex
      justify-content: center
      .tab-version-item
        margin: 0 15px
  .mySystem
    display: flex
    width: 100%
    height: 39px
    border-bottom: 1px solid #cacaca
    .mySystem-item
      color: #25a4bb
      font-size: 14px
      line-height: 39px
      padding-left: 20px
  .look
    color: #616161
    margin-top: .1rem
    padding: .14rem .1rem
    font-size: .24rem
    line-height: .32rem
    background: #fff
    .lookIcon
      font-size: .24rem
    em
      margin-left: .05rem
      font-weight: bold
  .main-nav
    .main-nav-items
      position: relative
      width: 300px
      height: 25px
      margin: 0 auto
      padding: 10px 10px 0 10px
      overflow: hidden
      display: flex
      .main-nav-item
        padding-left: 10px
        display: flex
        width: 65px
        .more
          font-size: 14px
          border-left: 1px solid #acacac
          padding-left: 12px
          color: #9e9e9e
          margin-top: 3px
          font-size: 12px
          height: 13px
          line-height: 13px
        .icon
          float: left
          width: 22px
          height: 22px
          background: url(//source.qunarzz.com/site/images/wap/touch/images/v2/images2x/nav_7.png) 0 0 no-repeat
          background-size: 175px 50px
        .hotel
          background-position: -25px 0
        .flat
          background-position: -150px 0
        .icon-text
          color: #9e9e9e;
          margin: 3px 0 0 5px;
          border-bottom: 1px solid #acacac;
          font-size: 12px;
          height: 13px
          line-height: 13px
</style>
