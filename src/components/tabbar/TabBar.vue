<template>
  <div class="tabbar">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: 'TabBar',
  }
</script>

<style scoped>
  .tabbar {
    display: flex;
    height: 49px;
    background-color: #f6f6f6;
    box-shadow: 0 -1px 1px #ccc;
  }
</style>
