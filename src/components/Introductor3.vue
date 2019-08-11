<template>
  <div class="company-introdution">
    <mt-navbar v-model="active">
      <mt-tab-item id="tab-container1">合作方式</mt-tab-item>
      <mt-tab-item id="tab-container2">合作流程</mt-tab-item>
    </mt-navbar>
    <mt-tab-container v-model="active">
      <mt-tab-container-item id="tab-container1">
        <ul>
          <li>1、分公司</li>
          <li>2、华亿旗下各品牌代理商</li>
          <li>3、个性定制服务</li>
        </ul>
      </mt-tab-container-item>
      <mt-tab-container-item id="tab-container2">
        <ul>
          <li>1、咨询</li>
          <li>2、意向确定</li>
          <li>3、签约</li>
          <li>4、打款</li>
          <li>5、运作</li>
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
