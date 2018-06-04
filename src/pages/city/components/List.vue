<template>
  <div class="city-list" ref="list">
   <div>
    <div class="type-city">
      <div class="type-city-title">热门城市</div>
      <ul class="type-city-items">
        <li class="type-city-item" v-for="item of hotCities" :key="item.id">{{item.name}}</li>
      </ul>
    </div>
    <div class="type-city" v-for="(item,key) of cities" :key="key">
      <div class="type-city-title">{{key}}</div>
      <ul class="type-city-items">
        <li class="type-city-item" v-for="it of item" :key="it.id">{{it.name}}</li>
      </ul>
    </div>
   </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  props: ['hotCities', 'cities'],
  mounted () {
    this.scroll = new Bscroll(this.$refs.list)
  }
}
</script>

<style lang="stylus" scoped>
.city-list
  position: absolute
  left: 0
  right: 0
  top: 1.7rem
  bottom: 0
  overflow: hidden
  .type-city-title
    font-size: .24rem;
    padding: .24rem .3rem
    background: #f3f3f3
  .type-city-items
    overflow: hidden
    zoom: 1
    position: relative
    &:before
      content: ""
      position: absolute
      width: 33.3%
      height: 100%
      left: 33.3%
      border-left: .02rem solid #ddd
      border-right: .02rem solid #ddd
    .type-city-item
      float: left
      width: 33.3%
      line-height: .9rem
      height: .9rem
      text-align: center
      border-bottom: .02rem solid #ddd
</style>
