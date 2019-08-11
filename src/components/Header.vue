<template>
  <div class="header">
    <img class="logo" alt="Vue logo" src="../assets/logo.png" />
    <h1>贵州华亿河山科技有限公司</h1>
    <img class="music" alt="music" src="../assets/music.png" />
    <audio id="music-audio" preload="metadata" loop="loop" src="../assets/bg.mp3" autoplay>
      <code>audio</code>
    </audio>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    // msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  font-size: 20px;
  padding-top: 8px;
  padding-left: 14px;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.logo {
  width: 47px;
  height: 54px;
  float: left;
}
.header {
  display: -webkit-flex;
  display: flex;
  justify-content: space-between;

  line-height: 50px;
  overflow: hidden;
  margin: 10px;
}
.music {
  width: 22px;
  height: 22px;
  -webkit-animation: rotate2d 1.2s linear infinite;
  animation: rotate2d 1.2s linear infinite;
  position: relative;
  top: 32px;
  left: 2px;
}
@-webkit-keyframes rotate2d {
  from {
    -webkit-transform: rotate(0deg);
  }
  to {
    -webkit-transform: rotate(360deg);
  }
}

@keyframes rotate2d {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
</style>
