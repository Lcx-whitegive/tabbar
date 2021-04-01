<template>
  <div>
    <tab-bar class="tabbar">
      <tab-bar-item link="/home" activeColor="deeppink">
        <img slot="itemIcon" src="~assets/img/tabbar/home.png" alt="">
        <img slot="itemIcon-active" src="~assets/img/tabbar/home-active.png" alt="">
        <div slot="itemName">首页</div>
      </tab-bar-item>
      <tab-bar-item link="/category" activeColor="deeppink">
        <img slot="itemIcon" src="~assets/img/tabbar/category.png" alt="">
        <img slot="itemIcon-active" src="~assets/img/tabbar/category-active.png" alt="">
        <div slot="itemName">分类</div>
      </tab-bar-item>
      <tab-bar-item link="/cart" activeColor="deeppink">
        <img slot="itemIcon" src="~assets/img/tabbar/cart.png" alt="">
        <img slot="itemIcon-active" src="~assets/img/tabbar/catr-active.png" alt="">
        <div slot="itemName">购物车</div>
      </tab-bar-item>
      <tab-bar-item link="/profile" activeColor="deeppink">
        <img slot="itemIcon" src="~assets/img/tabbar/profile.png" alt="">
        <img slot="itemIcon-active" src="~assets/img/tabbar/profile-active.png" alt="">
        <div slot="itemName">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
  import TabBar from 'components/tabbar/TabBar'
  import TabBarItem from 'components/tabbar/TabBarItem'
  export default {
    name: 'MainTabBar',
    components: {
      TabBar,
      TabBarItem
    }
  }
</script>

<style scoped>
</style>
