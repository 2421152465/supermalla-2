<template>
  <div>
    <tab-ber>
      <tab-bar-item path='/home'>
        <img slot="item-icon" src="@/assets/img/tabbar/maozi1.png" alt="">
        <img slot="item-icon-active" src="@/assets/img/tabbar/maozi2.png" alt="">
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path='/profile'>
        <img slot="item-icon" src="@/assets/img/tabbar/daiz1.png" alt="">
        <img slot="item-icon-active" src="@/assets/img/tabbar/daiz2.png" alt="">
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path='/category'>
        <img slot="item-icon" src="@/assets/img/tabbar/qiu1.png" alt="">
        <img slot="item-icon-active" src="@/assets/img/tabbar/qiu2.png" alt="">
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path='/bat'>
        <img slot="item-icon" src="@/assets/img/tabbar/zuis1.png" alt="">
        <img slot="item-icon-active" src="@/assets/img/tabbar/zuis2.png" alt="">
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-ber>
  </div>
</template>

<script>
import TabBarItem from '../../common/tabber/TabBarItem.vue'
import TabBer from '../../common/tabber/TabBer.vue'

export default {
  components: { TabBer, TabBarItem },
  name:'MainTabBar'
}
</script>

<style>

</style>