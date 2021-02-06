<template>
  <div id="app">
    <!--上床成功-->
    <router-view/>
    <main-tab-bar/>
  </div>
</template>
<script>
import MainTabBar from '@/components/content/mainTabbar/MainTabBar.vue'
export default {
  components: { MainTabBar },
  
}
</script>
<style>
@import url(./assets/css/base.css);
</style>
