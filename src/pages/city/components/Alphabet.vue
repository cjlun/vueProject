<template>
  <div class="city-alphabet" ref="alphabet">
    <div class="alphabet-item" v-for="item of alphabets" :key="item" :ref="item" @click="handleAlphabetClick" @touchstart="touchstart" @touchmove="touchmove" @touchend="touchend">{{item}}</div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: ['alphabets'],
  data () {
    return {
      status: false
    }
  },
  computed: {
    positionA () {
      return this.$refs.A[0].offsetTop
    }
  },
  methods: {
    handleAlphabetClick (e) {
      this.$emit('alphabetChange', e.target.innerHTML)
    },
    touchstart () {
      this.status = true
    },
    touchmove (e) {
      if (this.status) {
        const positionY = e.touches[0].clientY
        const index = Math.floor((positionY - this.positionA - 84) / 20)
        if (index >= 0 && index <= 21) {
          this.$emit('alphabetChange', this.alphabets[index])
        }
      }
    },
    touchend () {
      this.status = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .city-alphabet
    z-index: 2
    position: absolute
    top: 0
    bottom: 0
    right: 0
    width: .55rem
    display: flex
    flex-direction: column
    justify-content: center
    text-align: center
    .alphabet-item
      height: .4rem
      line-height: .4rem
      font-size: .24rem
      color: #00bcd4
</style>
