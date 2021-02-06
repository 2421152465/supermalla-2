<template>
  <div id="home">
    <nav-bar class="home-nav">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-swiper :banners='banners'></home-swiper>
    <recommend-view :recommend="recommends"></recommend-view>
    <feature-view/>
    <tab-control :titles="['流行','精选','新款']"/>
  </div>
</template>

<script>
import NavBar from '@/components/common/navbar/NavBar.vue'
import TabControl from '@/components/content/tabControl/TabControl.vue'

import HomeSwiper from './childComps/HomeSwiper.vue'
import RecommendView from './childComps/RecommendView.vue'
import FeatureView from './childComps/FeatureView.vue'
//数据请求
import {getHomeMultidata} from '@/network/home.js'


export default {
  components: { NavBar,HomeSwiper, RecommendView, FeatureView,TabControl },
  data(){
    return{
      banners:[],
      recommends:[]
    }
  },
  created(){
    //创建完调用，请求数据
    this.getHomeMultidata();
  },
  methods:{
    //请求数据
    getHomeMultidata(){
      getHomeMultidata().then(res=>{
        this.banners = res.data.data.banner.list
        this.recommends = res.data.data.recommend.list
      })
    }
  }
}
</script>

<style>
  #home{
    padding-top: 44px;
    padding-bottom: 49px;
  }
  .home-nav{
    background-color: var(--color-text);
    color: white;
    font-weight:bold;
    position:fixed;
    right: 0;
    left: 0;
    top: 0;
    z-index: 9;
  }
</style>