<template>
  <div class="city-header">
    <div class="city-header-title">
      <router-link tag="span" to="/" class="iconfont city-header-icon">&#xe624;</router-link>
      <h1 class="city-header-name">城市选择</h1>
    </div>
    <div class="city-header-tab">
      <ul>
        <li class="active">境内</li>
        <li>境外·港澳台</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~style/ellipsis.styl'
.city-header
  position: relative
  background:#00bcd4
  .city-header-name
    margin: 0 1rem
    font-size: .32rem
    line-height: .88rem
    color: #fff
    text-align: center
    ellipsis()
  .city-header-icon
    position: absolute
    left: 0
    top: 0
    width: .8rem
    height: .88rem
    line-height: .88rem
    text-align: center
    color: #fff
.city-header-tab
  height: .4rem
  line-height: .4rem
  padding: .2rem 1rem
  ul
    border: 1px solid #fff
    border-radius: .03rem
    display: flex
    color: #fff
    li
      flex: 1
      text-align: center
    .active
      background: #fff
      color: #00bcd4
</style>
