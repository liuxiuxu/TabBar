<template>
  <div id="app">
    <div class="content">
      <router-view></router-view>
    </div>
    <tab-bar>
      <tab-bar-item path='/home' activeColor="skyblue">
        <div slot='item-icon' class="iconfont">&#xe674;</div>
        <img slot='item-icon-active' src="./assets/img/首页.png" alt="">
        <div slot='item-text'>首页</div>
      </tab-bar-item>
      <tab-bar-item path='/classify' activeColor="skyblue">
        <div slot='item-icon' class="iconfont">&#xe7f9;</div>
        <img slot='item-icon-active' src="./assets/img/分类.png" alt="">
        <div slot='item-text'>分类</div>
      </tab-bar-item>
      <tab-bar-item path='/cart' activeColor="skyblue">
        <div slot='item-icon' class="iconfont">&#xe63b;</div>
        <img slot='item-icon-active' src="./assets/img/购物车.png" alt="">
        <div slot='item-text'>购物车</div>
      </tab-bar-item>
      <tab-bar-item path='/mine' activeColor="skyblue">
        <div slot='item-icon' class="iconfont">&#xe682;</div>
        <img slot='item-icon-active' src="./assets/img/我的.png" alt="">
        <div slot='item-text'>我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>
<script>
import TabBar from './components/tabbar/TabBar'
import TabBarItem from './components/tabbar/TabBarItem.vue'
  export default {
    name:'App',
    components:{
      TabBar,
      TabBarItem
    }
  }
</script>
<style lang="less">
  @import 'assets/css/iconfont.css';
  @import './assets/css/base.css';
  .content{
    font-size: 30px;
  }
</style>
