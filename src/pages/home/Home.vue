<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
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
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon,
    HomeHot,
    HomeLike,
    HomeWeekend,
    HomeFooter
  }
}
</script>

<style lang="stylus" scoped>
</style>
