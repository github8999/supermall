<template>
  <div class="app">
    {{a.name}}-{{a.age}}
    <keep-alive exclude="Detail"><router-view></router-view></keep-alive>
    
    <main-tab-bar/>
    <icon></icon>
    <svg-icon></svg-icon>
  </div>
</template>

<script>
import MainTabBar from 'components/content/mainTabbar/MainTabBar'
import Icon from 'components/content/Icon/Icon.vue'
import SvgIcon from 'components/content/Icon/svg.vue'
export default {
  name: 'App',
  data() { 
    return {
      a: {
        name: '张三'
      }
    }
  },
  created() {
    console.log(this.a)
  },
  components:{
    MainTabBar,
    Icon,
    SvgIcon,
  }
 }
</script>

<style scoped>
@import "./assets/css/base.css";
</style>