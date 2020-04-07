<template>
  <div id="app">
    <MainTabBar></MainTabBar>
    <router-view></router-view>
  </div>
</template>

<style>
  @import "./assets/css/base.css";

</style>
<script>
  import MainTabBar from "./components/content/maintabbar/MainTabBar"

  export default {
    components: {MainTabBar}
  }
</script>