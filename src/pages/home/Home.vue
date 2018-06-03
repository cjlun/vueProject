<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper :swiper="swiper"></home-swiper>
    <home-icon :icon="icon"></home-icon>
    <home-hot></home-hot>
    <home-like></home-like>
    <home-weekend></home-weekend>
    <home-footer></home-footer>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcon from './components/Icon'
import HomeHot from './components/Hot'
import HomeLike from './components/Like'
import HomeWeekend from './components/Weekend'
import HomeFooter from './components/Footer'
import axios from 'axios'
export default {
  name: 'Home',
  data () {
    return {
      swiper: [],
      icon: []
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon,
    HomeHot,
    HomeLike,
    HomeWeekend,
    HomeFooter
  },
  methods: {
    getHomeInfo () {
      axios.get('/static/serverData/home.json').then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      this.swiper = res.data.data.swiper
      this.icon = res.data.data.icon
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style lang="stylus" scoped>
</style>
