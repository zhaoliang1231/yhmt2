<template>
    <div class="Like">
      <div class="container">
        <div class="like_title">
            <div class="title_l">
              <h4>猜你喜欢</h4>
              <span>根据你的浏览记录推荐的商品</span>
            </div>
            <div class="another">
              <span>换一批</span>
              <span class="refrsh_icon"></span>
            </div>
        </div>
        <div class="like_content">
          <ul>
            <li v-for="item in list">
              <div class="like_content_lists">
                <img src="../static/img/banner4.jpg" alt="">
                <div class="like_content_c">
                  <span>{{item.title}}</span>
                </div>
                <div class="like_monery">
                  <h5>￥{{item.m}}</h5>
                  <label>￥{{item.m2}}</label>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
        name: "Like",
      data (){
          return{
            list:[
              {title:"实物商品标题实物商品标题实物商品标实物商品标题实物商品标题",m:"999.00",m2:"1999.00"},
              {title:"实物商品标题实物商品标题实物商品标实物商品标题实物商品标题",m:"999.00",m2:"1999.00"},
              {title:"实物商品标题实物商品标题实物商品标实物商品标题实物商品标题",m:"999.00",m2:"1999.00"},
              {title:"实物商品标题实物商品标题实物商品标实物商品标题实物商品标题",m:"999.00",m2:"1999.00"},
              {title:"实物商品标题实物商品标题实物商品标实物商品标题实物商品标题",m:"999.00",m2:"1999.00"},
            ]
          }
      }
    }
</script>

<style scoped>
  .like_title{
    width: 100%;
    height: 55px;

  }
  .title_l{
    width: 699px;
    height: 55px;
    line-height: 55px;
    float: left;
  }
  .title_l h4{
    display: inline-block;
    color: #EB193E;
    font-weight: bold;
  }
  .title_l span{
    display: inline-block;
    font-size: 14px;
  }
  .like_title .another{
    width: 200px;
    height: 55px;
    line-height: 70px;
    text-align: right;
    font-size: 12px;
    float: right;
  }
  .like_title .another .refrsh_icon{
    display: inline-block;
    width: 22px;
    height: 15px;
    vertical-align: -4px;
    background: url("../static/img/icon.png")no-repeat -20px 0;
  }
  .like_content{
    width: 100%;
    height: 360px;
    border: 1px solid #ddd;
    border-top: 3px solid #EB193E;
  }
  .like_content ul{
    width: 1140px;
    height: 310px;
    margin: 25px auto;
  }
  .like_content ul li{
    width: 228px;
    height: 310px;
    float: left;
    border: 1px solid #ddd;
  }
  .like_content_lists {
    width: 208px;
    height: 300px;
    margin: 10px auto  ;
  }
  .like_content_lists img{
    width: 208px;
    height: 208px;
  }
  .like_content_lists .like_content_c{
    font-size: 14px;
    width: 208px;
    height: 40px;
    margin-top: 10px;
    overflow: hidden;
    text-overflow:ellipsis;
  }
  .like_monery{
    width: 208px;
    height: 40px;
    line-height: 40px;
  }
  .like_content_lists h5{
    color: #EB193E;
    font-weight: bold;
    display: inline-block;
  }
  .like_content_lists label{
    font-size: 14px;
    text-decoration: line-through;
  }
</style>
