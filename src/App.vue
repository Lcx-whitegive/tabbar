<template>
  <div id="app">
    <main-tab-bar></main-tab-bar>
    <router-view/>
  </div>
</template>

<script>
import MainTabBar from 'components/tabbar/MainTabBar'
export default {
  name: 'App',
  components: {
    MainTabBar
  }
}
</script>

<style>
  @import "./assets/css/base.css";
  .tabbar {
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
  }
</style>
