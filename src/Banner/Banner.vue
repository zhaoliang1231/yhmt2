<template>
    <div class="container-fluid">
      <div class="container">
        <div class="container_bar">
          <ul class="container_img">
            <li v-for='item in list'>
              <img  :src="item">
            </li>
          </ul>
          <div class="toLeft">&lt;</div>
          <div class="toRight">&gt;</div>
          <!-- 创建小圆点 -->
          <div class="circular">
            <li class="active">1</li>
            <li>2</li>
            <li>3</li>
          </div>
        </div>
        <div class="article">
            <div class="article_title">
              <span class="article_zx">文章咨询</span>
              <div>
                <span class="article_gd" style="font-size: 12px">更多 ></span>
              </div>
            </div>
          <div class="article_content" v-for="item in list2">
            <div class="article_content_list">
              <div class="article_content_title">{{item.title}}</div>
              <div class="article_content_con">{{item.content}}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
  import banner1 from '../static/img/banner1.jpg'
  import banner3 from '../static/img/banner3.jpg'
  import banner4 from '../static/img/banner4.jpg'
    export default {
        name: "Banner",
      data(){
          return{
            list: [banner1,banner3,banner4,banner1],
            list2:[
              {title:"【公告】",content:"此处是文章标题,如有超出asdsadasd"},
              {title:"【活动】",content:"此处是文章标题,如有超出asdsadasd"},
              {title:"【公告】",content:"此处是文章标题,超出隐藏部分"},
              {title:"【健康】",content:"牛肝菌的使用方法和营养价值"},
              {title:"【科普】",content:"虫草花怎么吃？虫草花怎么吃？"},
              {title:"【活动】",content:"卖茶叶送大众轿车"},
              {title:"【公告】",content:"他们不会告诉你菠萝可以"},
              {title:"【健康】",content:"牛肝菌的使用方法和营养价值"},
              {title:"【科普】",content:"虫草花怎么吃？虫草花怎么吃？"},
              {title:"【活动】",content:"卖茶叶送大众轿车"},
              {title:"【公告】",content:"他们不会告诉你菠萝可以"}
            ]
          }

      },
      mounted(){
        function test() {
          var index = 0;
          //每隔1500毫秒自动轮播一次
          var id = setInterval(play, 2000);

          function change(currentIndex) {
            //小圆点对应切换
            $(".circular li").removeClass("active").eq(currentIndex).addClass("active");
            //切换图片
            $(".container_img li").hide().eq(currentIndex).show();
          }
          //轮播方法
          function play() {
            index++;
            if (index > 2) {
              index = 0;
            }
            change(index);
          }
          //小圆点点击事件
          $(".circular li").click(function () {
            index = $(this).index();

            change(index);
          });

          //当鼠标移动到容器中，暂停轮播
          $(".container_bar").hover(function () {
            $(".toLeft").show();
            $(".toRight").show();
            clearInterval(id);
          }, function () {
            $(".toLeft").hide();
            $(".toRight").hide();
            id = setInterval(play, 2000);
          });

          //点击左右切换图片

          $(".toLeft").click(function () {
            index--;
            if (index < 0) {
              index = 2;
            }
            change(index);
          });

          $(".toRight").click(function () {
            index++;
            if (index > 2) {
              index = 0;
            }
            change(index);
          });
        }
        test();
      }
    }
</script>

<style scoped >

  .article{
    width: 20%;
    height: 370px;
    margin-left: 2px;
    margin-top: 2px;
    border: 1px solid #ddd;
    float: left;
  }
  .article_title{
    display: flex;
    height: 40px;
    line-height: 40px;
    align-content: center;
    justify-content: space-between;
    font-size: 12px;
    border-bottom: 1px solid #ddd;
  }
  .article_zx{
    display: inline-block;
    padding-left: 10px;
    font-weight: bold;
  }
  .article_gd{
    display: inline-block;
    font-size: 14px;
    padding-right: 10px;
    color: #ff2d52;
  }
.article_content_list{
  height: 30px;
  line-height: 36px;
  font-size: 12px;
  display: flex;
  justify-content: space-between;
}
  .article_content_title{
    width: 60px;
    padding-left: 6px;
  }
.article_content_con{
  width: 130px;
  padding-right: 6px;
  overflow: hidden;
  text-overflow:ellipsis;
  white-space:nowrap
}
.container_bar {
  width: 63%;
  float: left;
  height: 371px;
  margin-left: 195px;
  position: relative;
}

ul {
  width: 63%;
}

ul,
img {
  width:100%;
  height: 371px;
}

ul li {
  list-style: none;
  position: absolute;
}

.toLeft,
.toRight {
  font-size: 50px;
  width: 40px;
  height: 40px;
  display: inline-block;
  position: absolute;
  z-index: 150;
  text-align: center;
  line-height: 40px;
  background: rgba(2, 2, 2, .3);
  top: 180px;
  color: white;
  cursor: pointer;
  display: block;
}
.toLeft{
  left: 15px;
}
.toRight {
  right: 15px;
}

.circular {
  position: absolute;
  bottom: -20px;
  left: 300px;
  z-index: 100;
  width: 300px;
  height: 50px;
  line-height: 50px;
}

.circular li {
  list-style: none;
  /*display: inline-block;*/
  width: 15px;
  height: 15px;
  line-height: 15px;
  text-align: center;
  color: white;
  float: left;
  border-radius: 100%;
  margin-left: 15px;
  cursor: pointer;
  background: #5E5955;
  font-size: 12px;
}

.circular .active {
  background: #ff2d52;
}

</style>
