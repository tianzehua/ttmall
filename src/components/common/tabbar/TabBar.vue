<template>
  <div id="tab-bar">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: "Tabbar",
    components: {}
  }
</script>

<style scoped>
  /* id 的样式配置 */
  #tab-bar {
    display: flex; /*水平排列*/
    height: 49px; /* tabbar的高度 */

    /* tabbar放置在下方 */
    position: fixed;
    left: 0px;
    right: 0px;
    bottom: 0px;

    /* 改变tabbar的背景颜色以及制作分界线 */
    background-color: #f6f6f6;
    box-shadow: 0 -3px 1px rgba(100,100,100,.1);
  }
</style>