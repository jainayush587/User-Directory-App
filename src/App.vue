<template>
  <div id="app">
    <nav-bar></nav-bar>
    <router-view />
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
export default {
  name: "App",
  components:{
    NavBar,
  }
}
</script>

<style lang="less">
body {
  background-color: #f0f2fa;
  font-family: "PT Sans", "Helvetica Neue", "Helvetica", "Roboto", "Arial", "sans-serif";
  .container {
    padding-right: 15px;
    padding-left: 15px;
    margin-right: auto;
    margin-left: auto;
  }
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

@media (min-width: 768px) {
  .container {
    width: 750px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 970px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1170px;
  }
}
</style>
