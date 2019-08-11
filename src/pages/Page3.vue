<template>
  <div>
    <Header/>
    <ShowImg/>
    <Introductor/>
  </div>
</template>

<script>
import Header from '../components/Header.vue';
import ShowImg from '../components/ShowImg.vue';
import Introductor from '../components/Introductor3.vue';

export default {
  name: "Page3",
  props: {
    // msg: String
  },
  components: {
    Header,
    ShowImg,
    Introductor,
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
