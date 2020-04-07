<template>
  <div id="maint-tab-bar">
    <!-- 通过父组件传递path，子组件通过propes来接收父组件的值 -->
    <tabbar>
      <tab-bar-item path="/home" colors="red">
        <img src="~assets/img/tabbar/home.svg" slot="item-icon">
        <img src="~assets/img/tabbar/home_active.svg" slot="item-icon-active">
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category" colors="red">
        <img src="~assets/img/tabbar/category.svg" slot="item-icon">
        <img src="~assets/img/tabbar/category_active.svg" slot="item-icon-active">
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/cart" colors="red">
        <img src="~assets/img/tabbar/shopcart.svg" slot="item-icon">
        <img src="~assets/img/tabbar/shopcart_active.svg" slot="item-icon-active">
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile" colors="red">
        <img src="~assets/img/tabbar/profile.svg" slot="item-icon">
        <img src="~assets/img/tabbar/profile_active.svg" slot="item-icon-active">
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tabbar>
  </div>
</template>

<script>
  import Tabbar from 'components/common/tabbar/TabBar'
  import TabBarItem from 'components/common/tabbar/TabBarItem'

  export default {
    name: "MainTabBar",
    components: {TabBarItem, Tabbar}
  }

</script>

<style scoped>

</style>