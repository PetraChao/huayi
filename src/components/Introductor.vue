<template>
  <div class="company-introdution">
    <mt-navbar v-model="selected">
      <mt-tab-item id="1">产品优势</mt-tab-item>
      <mt-tab-item id="2">政策支持</mt-tab-item>
      <mt-tab-item id="3">售后支持</mt-tab-item>
      <mt-tab-item id="4">促销物料支持</mt-tab-item>
      <mt-tab-item id="5">广告品牌支持</mt-tab-item>
      <!-- <mt-tab-item id="6">合作方式</mt-tab-item> -->
      <!-- <mt-tab-item id="7">合作流程</mt-tab-item> -->
    </mt-navbar>
    <mt-tab-container v-model="active">
      <mt-tab-container-item id="tab-container1">
        1、满足不同消费者的需求
        2、终端体验感十足
        3、产品稳定，不跳码
      </mt-tab-container-item>
      <mt-tab-container-item id="tab-container2">
        1、顶级政策共享，总部直签
        2、不压货
      </mt-tab-container-item>
      <mt-tab-container-item id="tab-container3">
        1、全天24小时即时服务
        2、提供产品知识培训，后台系统管理培训等
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
  name: "introductor",
  props: {
    // msg: String
  },
  data() {
    return {
      active: "tab-container1",
      selected: '1'
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
