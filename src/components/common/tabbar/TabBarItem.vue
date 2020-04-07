<template>
  <div class="tab-bar-item" @click="bkbutton">
    <!-- 具名插槽 -->
    <div v-if="!active">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-active"></slot>
    </div>
    <div :style="activecolor">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: "TabBarItem",
    data(){
      return {
       /* active :true*/
      }
    },
    props:{
      path:String,
      colors:{
        default: 'red',
        type:String
      }
    },
    computed:{
      active(){
        return this.$route.path.indexOf(this.path) != -1
      },
      activecolor(){
        return this.active ? {color : this.colors}:{}
      }
    },
    methods:{
      bkbutton(){
       /* console.log('router');*/
        this.$router.push(this.path);
      }
    }
  }
</script>

<style scoped>
  .tab-bar-item {
    flex: 1; /* 均等排列 */
    text-align: center; /*文字居中 */
    font-size: 14px;
  }
  .tab-bar-item img {
    height: 24px;
    width: 24px;
    margin-top: 3px;
    vertical-align: middle;
  }
  /*.actives {
    color: red;
  }*/


</style>