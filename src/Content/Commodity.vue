<template>
  <div class="Commodity">
    <div class="container">
      <div class="commodity_title">
        <ul>
          <li>精品推荐</li>
          <li>促销商品</li>
          <li>新品推荐</li>
        </ul>
        <div class="another">
          <span>换一批</span>
          <span class="refrsh_icon"></span>
        </div>
      </div>
      <div class="commodity_details">
        <ul>
          <li v-for="item in list" class="commodity_details_lists">
            <div class="commodity_details_list">
              <img src="../static/img/banner2.jpg" alt="">
              <span>{{item.title}}</span>
              <div class="monery">￥{{item.monery}}</div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
  import img from '../static/img/banner2.jpg'
    export default {
        name: "Commodity",
      data(){
          return{
            list:[
              {title:'实物商品标题实物商品标题',monery:'88.88',img:'../static/img/banner2.jpg'},
              {title:'实物商品标题实物商品标题',monery:'88.88',img:'../static/img/banner2.jpg'},
              {title:'实物商品标题实物商品标题',monery:'88.88',img:'../static/img/banner2.jpg'},
              {title:'实物商品标题实物商品标题',monery:'88.88',img:'../static/img/banner2.jpg'},
              {title:'实物商品标题实物商品标题',monery:'88.88',img:'../static/img/banner2.jpg'},
            ]
          }
      }
    }
</script>

<style scoped>
  ul{
    margin-bottom: 0;
  }

  .commodity_title{
    width: 100%;
    height: 55px;
    /*border: 1px solid;*/
  }
  .commodity_title ul {
    width: 699px;
    height: 55px;
    float: left;
  }
  .commodity_title ul li{
    width: 233px;
    height: 55px;
    line-height: 55px;
    text-align: center;
    float: left;
  }
  .commodity_title .another{
    width: 200px;
    height: 55px;
    line-height: 70px;
    text-align: right;
    font-size: 12px;
    float: right;
  }
  .commodity_title .another .refrsh_icon{
    display: inline-block;
    width: 22px;
    height: 15px;
    vertical-align: -4px;
    background: url("../static/img/icon.png")no-repeat -20px 0;
  }
  .commodity_details{
    clear: both;
    width: 100%;
    height: 278px;
    border-right: 1px solid #ddd;
    border-top: 1px solid #ddd;
    border-bottom: 1px solid #ddd;
  }
  .commodity_details ul{
    width: 100%;
    height: 278px;
    display: flex;
    justify-content: space-between;
  }
  .commodity_details_lists{
    width: 233px;
    height: 278px;
    border-left: 1px solid #ddd;
  }
  .commodity_details_list{
    width: 176px;
    height: 278px;
    margin: 0 auto;
    font-size: 14px;
    padding-top: 20px;
  }
  .commodity_details_lists .commodity_details_list img{
    width: 176px;
    height: 176px;
  }
  .commodity_details_list span{
    display: inline-block;
    padding-top: 10px;
    font-weight: bold;
  }
  .commodity_details_list .monery{
    color: #EB193E;
    font-weight: bolder;
  }
</style>
