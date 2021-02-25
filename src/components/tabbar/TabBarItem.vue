<template>
    <div class="item" @click='btnclick'>
      <div v-if="!isactive">
        <slot name='item-icon'></slot>
      </div>
      <div v-else>
       <slot name='item-icon-active'></slot>
      </div>
      <div :style="activeStyle">
         <slot name='item-text'></slot>
      </div>
    </div>
</template>

<script>
  export default {
    name:'TabBarItem',
    props:{
      path:String,
      activeColor:{
        type:String,
        default:'red'
      }
    },
    methods:{
      btnclick(){
        this.$router.replace(this.path)
      }
    },
    computed:{
      isactive(){
        return this.$route.path===this.path;
      },
      activeStyle(){
        return this.isactive?{color:this.activeColor}:{};
      }
    }
  }
</script>

<style lang="less" scoped>
  .item{
    flex: 1;
    text-align: center;
    font-size: 16px;
  }
  .iconfont{
    font-size: 26px;
  }
  img{
    display: inline-block;
    width: 30px;
    height: 30px;
  }
</style>