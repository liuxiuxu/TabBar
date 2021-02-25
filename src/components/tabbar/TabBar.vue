<template>
  <div>
    <div class="tabBar">
      <slot>
      </slot>
    </div>
  </div>
</template>

<script>
  export default {
    name:'TabBar',
  }
</script>

<style lang="less" scoped>
  .tabBar{
    display: flex;
    justify-content: space-around;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    height: 49px;
    background-color: #f6f6f6;
    box-shadow: 0 -1px 1px rgba(100,100,100,.2);
  }
</style>