<template>
 <div class="city">
  <city-header></city-header>
  <city-list :hotCities="hotCities" :cities="cities" :alphabets="alphabets"></city-list>
 </div>
</template>

<script>
import CityHeader from './components/Header'
import CityList from './components/List'
import axios from 'axios'
export default {
  name: 'City',
  components: {
    CityHeader,
    CityList
  },
  data () {
    return {
      hotCities: [],
      cities: [],
      alphabets: []
    }
  },
  methods: {
    getCityInfo () {
      axios.get('/static/serverData/city.json').then(this.getCityInfoSucc)
    },
    getCityInfoSucc (res) {
      if (res.data.ret && res.data.data) {
        this.hotCities = res.data.data.hotCities
        this.cities = res.data.data.cities
        for (let i in this.cities) {
          this.alphabets.push(i)
        }
      }
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style lang="stylus" scoped>
</style>
