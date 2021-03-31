<template>
  <div class="tabbar-item" @click="itemClick">
    <div v-if="!isActive">
      <slot name='itemIcon'></slot>
    </div>
    <div v-else>
      <slot name='itemIcon-active'></slot>
    </div>
    <div :class="{active: isActive}">
      <slot name="itemName"></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'TabBarItem',
    data() {
      return {
        isActive: true
      }
    },
    methods: {
      itemClick() {
        console.log('aaa');
      }
    }
  }
</script>

<style scoped>
  .tabbar-item {
    flex: 1;
    text-align: center;
  }
  .tabbar-item div {
    margin-top: 3px;
  }
  .tabbar-item img {
    width: 24px;
    height: 24px;
    vertical-align: middle;
  }
  .active {
    color: pink;
  }
</style>
