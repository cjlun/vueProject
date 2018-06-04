<template>
  <div class="header">
    <div class="header-back">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-search">
      <span class="iconfont search-icon">&#xe632;</span>输入城市/景点/游玩主题
    </div>
    <router-link tag="div" to="/city" class="header-select">
      {{$store.state.city}}<span class="iconfont">&#xe611;</span>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display: flex
    height: .88rem
    line-height: .88rem
    background: #00afc7
    .header-search
      padding-left: .2rem
      flex: 1
      color: #e4e7ea
      background: #fff
      height: .6rem
      margin: .14rem 0
      line-height: .6rem
      .search-icon
        padding-right: .1rem
        vertical-align: middle
    .header-back
      color: #fff
      padding: 0 .2rem
    .header-select
      color: #fff
      padding: 0 .22rem
</style>
