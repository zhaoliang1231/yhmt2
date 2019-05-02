<template>
  <div>
    <div class="container-fluid navigation_bar">
      <div @mouseenter="classifyToggle(true)"  @mouseleave="classifyToggle(false)" class="row container main_nav " :class="{current:flag}">
        <div class=" all_shop ">
          <div class="shop_all" style="width: 195px">
            <span class="shop_ico"></span>
            <span>全部商品分类</span>
          </div>
          <ul class="nav_classify_lists ">
            <li class="nav_classify_list">
              <span class="classify_myyp">母婴用品</span>
              <span class="ico_trangle"></span>
            </li>
            <li class="nav_classify_list">
              <span class="classify_myyp">美容护肤</span>
              <span class="ico_trangle"></span>
            </li>
            <li class="nav_classify_list">
              <span class="classify_myyp">生活家具</span>
              <span class="ico_trangle"></span>
            </li>
            <li class="nav_classify_list">
              <span class="classify_myyp">休闲食品</span>
              <span class="ico_trangle"></span>
            </li><li class="nav_classify_list">
            <span class="classify_myyp">进口食品</span>
            <span class="ico_trangle"></span>
          </li>
            <li class="nav_classify_list">
              <span class="classify_myyp">轻奢名品</span>
              <span class="ico_trangle"></span>
            </li>
            <li class="nav_classify_list">
              <span class="classify_myyp">母婴用品</span>
              <span class="ico_trangle"></span>
            </li>
          </ul>
        </div>


        <div class=" else_title">
          <ul>
            <li>
              <a href="">首页</a>
            </li>
            <li>
              <a href="">商城</a>
            </li>
            <li>
              <a href="">团购</a>
            </li>
            <li>
              <a href="">秒杀</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "NavigationBar",
    data(){
      return{
        //标记是否要改变导航栏状态
        isHide:false,
        //切换过程中改变导航分类是否显示
        flag:false
      }
    },
    mounted(){
      if(!this.isHide){
        this.flag = true;
      }
    },
    methods:{
      classifyToggle(stuats){
        if(this.isHide){
          this.flag = stuats;
        }

      }
    }
  }
</script>

<style scoped lang="less">
  @import "../static/css/common.less";

  .navigation_bar{
    height: 40px;
    background: @redLightColor;
    .main_nav{
      color: white;
      position: relative;
      &.current{
        .all_shop{
          background: @redShopColor;
        }
        .nav_classify_lists{
          display: block;
        }
      }
      .all_shop{
        height: 40px;
        text-align: center;
        line-height: 40px;
        background: @redLightColor;
        cursor: pointer;
        &:hover{
          background: @redShopColor;
        }
        .shop_ico{
          display: inline-block;
          width: 18px;
          height: 17px;
          margin-right: 10px;
          vertical-align: -4px;
          background: url("../static/img/icon.png")no-repeat;
        }
      }
      .nav_classify_lists{
        position: absolute;
        display: none;

        .nav_classify_list{
          width: 195px;
          height: 53px;
          line-height: 53px;
          border-bottom:1px solid @redShopColor ;
          background: @redLightColor;
          .classify_myyp{
            margin-left: -55px;
          }
          .ico_trangle{
            display: inline-block;
            width: 8px;
            height: 13px;
            float: right;
            margin-top: 22px;
            margin-right: 15px;
            background: url("../static/img/icon.png") no-repeat -70px 0;
          }
        }
      }
    }

    .container .else_title{
      height: 40px;
      ul li{
        display: inline-block;
        width: 100px;
        height: 40px;
        line-height: 40px;
        text-align: center;
        float: left;
        a{
          font-size: 16px;
          color: white;
        }
      }
    }
  }

</style>
