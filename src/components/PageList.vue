<template>
  <div>
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
        <!-- <div class="swiper-pagination"  slot="pagination"></div> -->
      
      </swiper>

      <div class="pagination">
        <img class="pre-button"  src="../assets/icon/pre.png" >
        <img class="next-button" src="../assets/icon/next.png">
      </div>
  </div>
  
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
    let screenHeight = window.screen.height
      return {
        swiperOption: {
          direction: 'vertical',
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          },
          height: screenHeight || 667,
          navigation: {
            nextEl: '.next-button',
            prevEl: '.pre-button',
          },
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
  },
  methods:{
    
  }
  
};
</script>
<style scoped>
.pagination{
  position: absolute;
  z-index: 99;
  display: flex;
  flex-direction: column;
  right: 5px;
  top:50%;
  width: 60px;
  height: 120px;
  
}

.pagination img{
    display: block;
    width:50px;
    height: 50px;
  }

.swiper-slide{
  /* height:400px; */
}

</style>