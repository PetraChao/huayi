<template>
  <div class="page-swipe">
    <mt-swipe :auto="4000">
      <mt-swipe-item><img src="../assets/swiper1.jpg"></mt-swipe-item>
      <mt-swipe-item><img src="../assets/swiper2.jpg"></mt-swipe-item>
      <mt-swipe-item><img src="../assets/swiper3.jpg"></mt-swipe-item>
    </mt-swipe>
  </div>
</template>

<script>
import { Swipe, SwipeItem } from "mint-ui";
import Vue from "vue";

Vue.component(Swipe.name, Swipe);
Vue.component(SwipeItem.name, SwipeItem);
export default {
  name: "ShoWImg",
  props: {
    // msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.page-swipe {
  height: 360px;
}

.page-swipe .mint-swipe-item {
  line-height: 360px;
}
.page-swipe .mint-swipe-item img{
  width: 100%;
  height: 360px;
}
.mint-swipe {
  height: 100%;
}
</style>
