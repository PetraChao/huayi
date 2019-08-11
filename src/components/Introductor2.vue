<template>
  <div class="company-introdution">
    <mt-navbar v-model="active">
      <mt-tab-item id="tab-container1">广告支持</mt-tab-item>
    </mt-navbar>
    <mt-tab-container v-model="active">
      <mt-tab-container-item id="tab-container1">
        <ul>
          <li>1、提供各种宣传广告图</li>
          <li>2、提供但不限于易拉宝、海报等宣传物料</li>
          <li>3、提供网站、微信公众号等引流服务</li>
          <li>4、提供不限于电梯等广告，加深品牌认知</li>
        </ul>
      </mt-tab-container-item>
    </mt-tab-container>
  </div>
</template>

<script>
import Vue from "vue";
import { TabContainer, TabContainerItem, Navbar, TabItem } from "mint-ui";

Vue.component(Navbar.name, Navbar);
Vue.component(TabItem.name, TabItem);
Vue.component(TabContainer.name, TabContainer);
Vue.component(TabContainerItem.name, TabContainerItem);
export default {
  name: "Introductor",
  props: {
    // msg: String
  },
  data() {
    return {
      active: "tab-container1",
      selected: "1"
    };
  },
  methods: {
    // selectTab: tabId => {
    //   console.log(tabId);
    // }
  }
};
</script>    

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
li {
  list-style-type: none;
  text-align: left;
}
</style>
