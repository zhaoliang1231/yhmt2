<template>
  <div class="top_nav container-fluid">
    <div class="container clearfix">
      <div class="topLeft">
        <a href="">设为首页</a>
        <span>|</span>
        <a href="">收藏本站</a>
      </div>
      <div class="topRight">
        <a href="">路人甲</a>
        <span>|</span>
        <a href="">退出登录</a>
        <span>|</span>
        <a href="">我的订单</a>
      </div>
    </div>


  </div>
</template>

<script>

    export default {
        name: "Top_Nav",
      data(){
          return{
          }
      }
    }
</script>

<style scoped lang="less">
  @import "~./static/css/common";
  .top_nav{
    height: 35px;
    border-bottom: 1px solid #ddd;
    background: #f7f7f7;
    line-height: 34px;
  }
  .topLeft{
    float: left;
  }
  .topRight{
    float: right;
  }
  .clearfix:after{
    content: '';
    clear: both;
  }
</style>
