<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {
  name: "app",
  methods: {
    resize() {
      var width = document.body.offsetWidth;
      var height = document.body.offsetHeight;
      var w_scale = width / 1230;
      var h_scale = height / 693;
      var app = document.getElementById("app");
      app.style.transform = "scale(" + w_scale + ", " + h_scale + ")";
    }
  },
  mounted() {
    this.resize();
    var that = this;
    window.addEventListener("resize", function() {
      setTimeout(function() {
        that.resize();
      }, 100);
    });
  }
};
</script>

<style lang="less">
@import "./assets/css/reset.css";

html {
  height: 100%;
  width: 100%;
}
body {
  margin: 0;
  padding: 0;
  min-height: 100%;
  width: 100%;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  min-height: 100%;
  background: url(./assets/images/bj.png) no-repeat 0 0;
  background-size: 100% 100%;
  position: relative;
  width: 1230px;
  height: 693px;
  transform-origin: left top 0px;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
