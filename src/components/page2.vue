<template>
  <div>
    <img class="srkl-img" src="../assets/srkl.gif" alt="">
  </div>
</template>

<script>
export default {
  name: 'page2',
  data () {
    return {
      num_bg_square: 10
    }
  },
  methods: {
    squareInit () {
      let sideLen = Math.random() * 90 + 10
      let speed = Math.random() * 6 + 9
      let square = document.createElement('div')
    }
  },
  mounted: {

  }
}
</script>

<style lang="less" rel="stylesheet/less">
.srkl-img{
  width: 60%;
  margin: 30% 20%;
}
</style>
