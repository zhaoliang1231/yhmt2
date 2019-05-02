<template>
    <div class="Special">
      <div class="container">
        <div class="special_title">
            <h5 class="special_title_tj">特价秒杀</h5>
            <span class="special_title_sy">本场还剩</span>
          <div class="special_title_time">
            <span>0</span>
            <span>1</span>
            <label>:</label>
            <span>2</span>
            <span>3</span>
            <label>:</label>
            <span>4</span>
            <span>5</span>
          </div>
        </div>
        <div class="special_content">
          <div class="special_content_left">
            <ul>
              <li v-for="i in list">
                <div class="special_content_detail">
                    <div class="special_content_detail_l">
                      <img src="../static/img/banner1.jpg" alt="">
                    </div>
                  <div class="special_content_detail_r">
                    <div>{{i.title}}</div>
                    <div>{{i.title1}}</div>
                    <div>
                      <span class="monery_l">￥{{i.m}}</span>
                      <span class="monery_r">￥{{i.m2}}</span>
                    </div>
                    <div>
                      <span class="special_content_detail_r_jdt"></span>
                      <span class="surplus">剩余{{i.num}}件</span>
                    </div>
                    <div class="rush_buy">立即抢买</div>
                  </div>
                </div>
              </li>
            </ul>
          </div>
          <div class="special_content_right">
            <div class="special_content_right_dj">点击进入></div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
        name: "Special",
      data (){
          return{
            list:[
              {title:"实物商品标题实物商品标题",title1:"实物商品标题实物商品",m:"123.44",m2:"1999.00",num:'130'},
              {title:"实物商品标题实物商品标题",title1:"实物商品标题实物商品",m:"123.44",m2:"1999.00",num:'130'},
              {title:"实物商品标题实物商品标题",title1:"实物商品标题实物商品",m:"123.44",m2:"1999.00",num:'130'},
              {title:"实物商品标题实物商品标题",title1:"实物商品标题实物商品",m:"123.44",m2:"1999.00",num:'130'},
              {title:"实物商品标题实物商品标题",title1:"实物商品标题实物商品",m:"123.44",m2:"1999.00",num:'130'},
              {title:"实物商品标题实物商品标题",title1:"实物商品标题实物商品",m:"123.44",m2:"1999.00",num:'130'},
            ]

          }
      }
    }
</script>

<style scoped>
  .special_title{
    width: 100%;
    height: 55px;
    line-height: 60px;
    border-bottom:3px solid #EB193E;
  }
  .special_title_tj{
    display: inline-block;
    font-weight: bolder;
    color: #EB193E;
  }
  .special_title_sy{
    font-size: 12px;
  }
  .special_title_time{
    display: inline-block;

  }
  .special_title_time span{
    width: 15px;
    height: 15px;
    text-align: center;
    font-size: 12px;
    color: white;
    background: #666;
    line-height: 15px;
    display: inline-block;
    border-radius: 100%;
    border: 1px solid;
  }
  .special_content{
    width:100%;
    height: 288px;
  }
  .special_content_left{
    width: 910px;
    height: 288px;
    float: left;
    border-right: 1px solid #ddd;

  }
  .special_content_left ul{
    width: 910px;
    height: 288px;
    display: flex;
    justify-content: space-around;
    flex-flow:wrap;
  }
  .special_content_left ul li{
    width: 303px;
    height: 144px;
    border-left: 1px solid #ddd;
    border-bottom: 1px solid #ddd;
  }
  .special_content_detail{
    width: 278px;
    height: 111px;
    margin: 15px auto;
  }
  .special_content_detail_l{
    width: 111px;
    height: 111px;
    float: left;
  }
  .special_content_detail_r{
    width: 165px;
    height: 111px;
    float: left;
    padding-left: 15px;
    font-size: 12px;
    color: #666;
  }
  .special_content_detail_r .monery_l{
    color: #EB193E;
    font-size: 14px;
    font-weight: bolder;
  }
  .special_content_detail_r .monery_r{
    text-decoration:line-through;

  }
  .special_content_detail_r .surplus{
    color: #FB9059;
  }

  .special_content_detail_r .rush_buy{
    width: 65px;
    height: 20px;
    color: white;
    background:#EB193E ;
    line-height: 20px;
    margin-top: 10px;
    text-align: center;
    cursor: pointer;
  }
  .special_content_detail_l img{
    width: 111px;
    height: 111px;
  }
  .special_content_right{
    width: 260px;
    height: 288px;
    float: left;
    background-color: #D4E9FA;

  }
  .special_content_right_dj{
    width: 80px;
    height: 30px;
    border-radius: 5px;
    font-size: 14px;
    color: white;
    text-align: center;
    line-height: 30px;
    margin: 150px auto;
    cursor: pointer;
    background-color: #A8B5BE;
  }
</style>
