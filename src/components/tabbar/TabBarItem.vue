<template>
  <div class="tabbar-item" @click="itemClick">
    <div v-if="!isActive">
      <slot name='itemIcon'></slot>
    </div>
    <div v-else>
      <slot name='itemIcon-active'></slot>
    </div>
    <div :style="isActiveColor">
      <slot name="itemName"></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'TabBarItem',
    data() {
      return {

      }
    },
    computed: {
      isActive() {
        return this.$route.path.indexOf(this.link) !== -1
      },
      isActiveColor() {
        return this.isActive ? {color: this.activeColor} : {}
      }
    },
    props: {
      link: {
        type: String,
      },
      activeColor: {
        type: String,
        default: "#fff"
      }
    },
    methods: {
      itemClick() {
        this.$router.replace(this.link)
      }
    },
    mounted() {
      this.aaa = this.$route.path
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
