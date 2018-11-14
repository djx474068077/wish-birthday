<template>
  <div>
    <swiper :options="swiperOption" ref="mySwiper">
      <swiper-slide>
        <page1></page1>
      </swiper-slide>
      <swiper-slide>
        <page2></page2>
      </swiper-slide>
      <swiper-slide>
        <page3></page3>
      </swiper-slide>
      <swiper-slide>
        <page4></page4>
      </swiper-slide>
      <!--<div class="swiper-pagination" >pagin</div>-->
      <!--<div class="swiper-button-prev">prev</div>-->
      <!--<div class="swiper-button-next" >next</div>-->
      <!--<div class="swiper-scrollbar" >scroll</div>-->
    </swiper>
  </div>
</template>

<script>
import {swiper, swiperSlide} from 'vue-awesome-swiper'
import page1 from './page1'
import page2 from './page2'
import page3 from './page3'
import page4 from './page4'
import 'swiper/dist/css/swiper.css'
export default {
  name: 'index',
  components: {swiper, swiperSlide, page1, page2, page3, page4},
  data () {
    return {
      swiperOption: {
        // notNextTick是一个组件自有属性，如果notNextTick设置为true，组件则不会通过NextTick来实例化swiper，也就意味着你可以在第一时间获取到swiper对象，假如你需要刚加载遍使用获取swiper对象来做什么事，那么这个属性一定要是true
        // notNextTick: true,
        autoplay: false,
        direction: 'vertical'
        // showIndicator: true,
        // pagination: '.swiper-pagination',
        // paginationClickable: true,
        // prevButton: '.swiper-button-prev',
        // nextButton: '.swiper-button-next',
      }
    }
  },
  computed: {
    swiper () {
      return this.$refs.mySwiper.swiper
    }
  },
  mounted () {
    console.log('mounted')
  }
}
</script>

<style lang="less" rel="stylesheet/less">
@red: #FF0000;
@pink: rgb(238, 156, 167);
@green: #00FF66;
@blur: #0099FF;
@black: #000000;
@white: #FFFFFF;
.swiper-slide {
  height: 100vh
}
.swiper-slide:nth-child(1){
  background: @black;
}
.swiper-slide:nth-child(2){
  background: @pink;
}
.swiper-slide:nth-child(3){
  background: @green;
}
.swiper-slide:nth-child(4){
  background: @blur;
}
.swiper-slide:nth-child(5){
  background: @red;
}
</style>
