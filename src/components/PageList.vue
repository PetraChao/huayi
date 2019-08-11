<template>
  <swiper :options="swiperOption" ref="mySwiper">
    <!-- slides -->
    <swiper-slide>I'm Slide 1</swiper-slide>
    <swiper-slide>I'm Slide 2</swiper-slide>
    <swiper-slide>I'm Slide 3</swiper-slide>
    <swiper-slide>I'm Slide 4</swiper-slide>
    <swiper-slide>I'm Slide 5</swiper-slide>
    <swiper-slide>I'm Slide 6</swiper-slide>
    <swiper-slide>I'm Slide 7</swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</template>

<script>
import Vue from "vue";
import VueAwesomeSwiper,{ swiper, swiperSlide } from 'vue-awesome-swiper' 
import 'swiper/dist/css/swiper.css'
Vue.use(VueAwesomeSwiper)
  // export default {
  //   data() {
  //     return {
  //       swiperOption: {
  //         direction: 'vertical',
  //         pagination: {
  //           el: '.swiper-pagination',
  //           clickable: true
  //         }
  //       }
  //     }
  //   }
  // }
export default {
name: 'PageList',
  components: {
      swiper,  
      swiperSlide  
  },  
  data() {
      return {
        swiperOption: {
          direction: 'vertical',
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          }
        }
      }
    },
  computed: {  
    swiper() {  
      return this.$refs.mySwiper.swiper;  
    }  
  }, 
  mounted () {  
    //可以使用swiper这个对象去使用swiper官网中的那些方法  
     console.log('this is current swiper instance object', this.swiper);
      // this.swiper.slideTo(0, 0, false);
  }   
};
</script>
<style scoped>
.swiper-slide{
  /* height:400px; */
}

</style>