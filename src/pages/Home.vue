<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
    <home-hot></home-hot>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcon from './components/Icon'
import HomeHot from './components/Hot'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon,
    HomeHot
  }
}
</script>

<style lang="stylus" scoped>
</style>
