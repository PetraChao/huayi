<template>
  <div class="company-introdution">
    <mt-navbar v-model="active">
      <mt-tab-item id="tab-container1">产品优势</mt-tab-item>
      <mt-tab-item id="tab-container2">政策支持</mt-tab-item>
    </mt-navbar>
    <mt-tab-container v-model="active">
      <mt-tab-container-item id="tab-container1">
        <ul>
          <li>1、满足不同消费者的需求</li>
          <li>2、终端体验感十足</li>
          <li>3、产品稳定，不跳码</li>
        </ul>
      </mt-tab-container-item>
      <mt-tab-container-item id="tab-container2">
        <ul>
          <li>1、顶级政策共享，总部直签</li>
          <li>2、不压货</li>
          <li>3、全天24小时即时服务</li>
          <li>4、提供产品知识培训，后台系统管理培训等</li>
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
