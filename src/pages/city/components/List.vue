<template>
  <div class="city-list" ref="list">
   <div>
    <div class="type-city">
      <div class="type-city-title">热门城市</div>
      <ul class="type-city-items">
        <router-link tag="li" to="/" class="type-city-item" v-for="item of hotCities" :key="item.id" @click.native="changeCity">{{item.name}}</router-link>
      </ul>
    </div>
    <div class="type-city" v-for="(item,key) of cities" :key="key" :ref="key">
      <div class="type-city-title">{{key}}</div>
      <ul class="type-city-items">
        <router-link tag="li" to="/" class="type-city-item" v-for="it of item" :key="it.id" @click.native="changeCity">{{it.name}}</router-link>
      </ul>
    </div>
   </div>
   <city-alphabet :cities="cities" :alphabets="alphabets" @alphabetChange="alphabetChange"></city-alphabet>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
import CityAlphabet from './Alphabet'
export default {
  name: 'CityList',
  props: ['hotCities', 'cities', 'alphabets'],
  data () {
    return {
      alphabet: ''
    }
  },
  components: {
    CityAlphabet
  },
  watch: {
    alphabet () {
      this.scroll.scrollToElement(this.$refs[this.alphabet][0])
    }
  },
  methods: {
    alphabetChange (alphabet) {
      this.alphabet = alphabet
    },
    changeCity (e) {
      this.$store.commit('changeCity', e.target.innerText)
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.list,{click: true})
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
      position: relative
      z-index: 10
      float: left
      width: 33.3%
      line-height: .9rem
      height: .9rem
      text-align: center
      border-bottom: .02rem solid #ddd
</style>
