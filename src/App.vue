<!-- 公共入口视图 -->
<!-- 首页样式与shop页样式有冲突 -->

<!-- html部分 -->
<template>
  <div id="app">
    <Header></Header>
    <div class="Header-box">占位盒子</div>
    <router-view></router-view>
    <Footer></Footer>
  </div>
</template>

<!-- js部分 -->
<script>
  // 导入购物监听
  import connect from '../static/js/connect.js'
  import shopTools from '../static/js/shopTools.js'

  export default {
    name: 'App',
    data(){
      return {
        title: ""
      }
    }
  }
</script>

<!-- css部分 -->
<style scoped>
  .Header-box{
    height: 40px;
  }
</style>
