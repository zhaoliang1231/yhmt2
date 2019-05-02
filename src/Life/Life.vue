<template>
  <div class="Life">

    <div class="Maternal">
      <div class="container">
        <div class="maternal_title">
          <div class="maternal_title_left">
            <h4>3F</h4>
            <h4 style="font-weight: bolder">生活家具</h4>
          </div>
          <div class="maternal_title_right">
            <ul>
              <li>童装童鞋</li>
              <li>营养店铺</li>
              <li>洗发用品</li>
              <li>育儿用品</li>
            </ul>
          </div>
        </div>
        <div class="maternal_content">
          <div class="maternal_content_l">
            <ul>
              <li>营养辅食</li>
              <li>洗护用品</li>
              <li>营养辅食</li>
              <li>营养辅食</li>
              <li>洗护用品</li>
              <li>营养辅食</li>
            </ul>
          </div>
          <div class="maternal_content_c">
            <ul>
              <li class="clearfix" v-for="i in list">
                <div class="maternal_content_box">
                  <img :src="i.img" alt="">
                  <span>{{i.title1}}</span>
                  <span>{{i.title2}}</span>
                  <span class="maternal_monery">￥{{i.m}}</span>
                </div>
              </li>
            </ul>
          </div>
          <div class="maternal_content_r clearfix">
            <div class="maternal_box_r">
              <span class="r_title">最新热卖</span>
              <ul>
                <li v-for="item in list1">
                  <img src="../static/img/banner1.jpg" alt="">
                  <div class="content_r">
                    <span class="content_r_t">{{item.title}}</span>
                    <label style="display: inline-block">￥{{item.monery}}</label>
                    <div style="display: inline-block;font-size: 12px; text-decoration: line-through">￥{{item.m2}}</div>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
  import banner1 from "../static/img/banner1.jpg"
  import banner2 from "../static/img/banner2.jpg"
  import banner3 from "../static/img/banner3.jpg"
  import banner4 from "../static/img/banner4.jpg"
  export default {
    name: "Life",
    data () {
      return{
        list:[{title1:"实物商品标题实物商品标题",title2:"实物商品标题",m:"123.44",img:banner1},
          {title1:"实物商品标题实物商品标题",title2:"实物商品标题",m:"123.44",img:banner2},
          {title1:"实物商品标题实物商品标题",title2:"实物商品标题",m:"123.44",img:banner3},
          {title1:"实物商品标题实物商品标题",title2:"实物商品标题",m:"123.44",img:banner4},
          {title1:"实物商品标题实物商品标题",title2:"实物商品标题",m:"123.44",img:banner1},
          {title1:"实物商品标题实物商品标题",title2:"实物商品标题",m:"123.44",img:banner2},
          {title1:"实物商品标题实物商品标题",title2:"实物商品标题",m:"123.44",img:banner3},
          {title1:"实物商品标题实物商品标题",title2:"实物商品标题",m:"123.44",img:banner4}
        ],
        list1:[
          {title:"实物商品标题实物商品",monery:"123.45",m2:"199"},
          {title:"实物商品标题实物商品",monery:"123.45",m2:"199"},
          {title:"实物商品标题实物商品",monery:"123.45",m2:"199"},
          {title:"实物商品标题实物商品",monery:"123.45",m2:"199"},
          {title:"实物商品标题实物商品",monery:"123.45",m2:"199"},
          {title:"实物商品标题实物商品",monery:"123.45",m2:"199"},
        ]
      }
    }
  }
</script>

<style scoped>
  .maternal_title{
    width: 100%;
    height: 55px;
    line-height: 55px;
    border-bottom:3px solid #EB193E;
  }
  .maternal_title_left{
    width: 40%;
    height: 55px;
    float: left;
  }
  .maternal_title h4{
    display: inline-block;
    color: #EB193E;
  }
  .maternal_title_right{
    width:60% ;
    height: 55px;
    line-height: 75px;
    float: right;
  }
  .maternal_title_right ul{
    display: flex;
    justify-content:flex-end;
  }
  .maternal_title_right ul li{
    width:70px;
    height: 55px;
    font-size: 12px;
    text-align: center;
    float: left;
  }

  .maternal_content{
    width: 100%;
    height: 500px;
    display: table;
    border-left: 1px solid #ddd;
    border-right: 1px solid #ddd;
  }
  .maternal_content_l{
    width: 260px;
    height: 500px;
    float: left;
    background: url("../static/img/banner4.jpg")no-repeat;
    background-size: 100% 100%;
  }
  .maternal_content_l ul{
    width: 100%;
    height: 150px;
    display: flex;
    margin: 300px auto;
    justify-content: center;
    flex-flow: wrap;
  }
  .maternal_content_l ul li{
    width: 70px;
    height: 70px;
    line-height: 70px;
    text-align: center;
    border-radius: 100%;
    margin-left: 5px;
    float: left;
    background: white;
    font-weight: bolder;
    cursor: pointer;
    font-size: 14px;
  }
  .maternal_content_l ul li:hover{
    background:#F1E1E1;
    color: #EB193E;
  }
  .maternal_content_c{
    width: 700px;
    height: 500px;
    float: left;
  }
  /*//定义一个clearfix类 解决margin塌陷*/
  .clearfix::before{
    content: "";
    display: table;
  }
  .maternal_content_c ul{
    width: 100%;
    height: 500px;
    display: flex;
    justify-content: space-between;
    flex-flow: wrap;
  }
  .maternal_content_c ul li{
    width: 175px;
    height: 250px;
    font-size: 12px;

    border-bottom: 1px solid #ddd;
    border-right: 1px solid #ddd;
  }
  .maternal_content_box{
    width:155px;
    height: 220px;
    margin: 14px auto;
  }
  .maternal_content_box span{
    display: block;
    margin-top: 3px;
  }
  .maternal_monery{
    font-size: 14px;
    color: #EB193E;
    font-weight: bolder;

  }
  .maternal_content_c img{
    width: 155px;
    height: 155px;
  }
  .maternal_content_r{
    width: 206px;
    height: 500px;
    float: left;
    border-bottom: 1px solid #ddd;

  }
  .maternal_box_r{
    width: 92%;
    height: 500px;
    margin: 0 auto;
  }
  .maternal_box_r span{
    width: 100%;
    height: 30px;
    line-height: 30px;
    display: inline-block;
    font-size: 12px;

  }
  .maternal_box_r ul{
    border-top: 1px solid #dddddd;

  }
  .maternal_box_r ul li{
    width: 189px;
    height: 78px;
    border-bottom: 1px solid #ddd;
  }
  .maternal_box_r ul li img{
    width: 60px;
    height: 60px;
    margin-top: 9px;
    float: left;
  }
  .content_r{
    width: 110px;
    height: 60px;
    margin-left: 10px;
    margin-top: 9px;
    float: left;

  }
  .content_r_t{
    overflow: hidden;
    text-overflow:ellipsis;
    white-space:nowrap
  }
  .content_r label{
    font-weight: bold;
    color: #EB193E;
  }
</style>
