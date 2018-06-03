<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
    <home-hot></home-hot>
    <home-like></home-like>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcon from './components/Icon'
import HomeHot from './components/Hot'
import HomeLike from './components/Like'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon,
    HomeHot,
    HomeLike
  }
}
</script>

<style lang="stylus" scoped>
</style>
