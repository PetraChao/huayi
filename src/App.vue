<template>
  <div id="app">
    <PageList/>
    <!-- <Header msg="Welcome to Your Vue.js App"/> -->
    <!-- <ShowImg /> -->
    <!-- <Introductor/> -->
  </div>
</template>

<script>
import PageList from './components/PageList.vue';
import Header from './components/Header.vue';
import ShowImg from './components/ShowImg.vue';
import Introductor from './components/Introductor.vue';
export default {
  name: 'app',
  components: {
    // Header,
    PageList,
    // ShowImg,
    // Introductor,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body{
  height: 100%;
  overflow: hidden;
}
</style>
