<template>
    <div class="Footer">
      <div class="container-fluid">
        <div class="container footer_content">
          <ul>
            <li>
              <div class="footer_logo_box">
                <div class="box_logo_l">
                  <span class="footer_logo">正</span>
                </div>
                <div class="box_logo_r">
                  <span class="zmbz">正品保障</span>
                  <div>100%正品商城</div>
                </div>
              </div>
            </li>
            <li>
              <div class="footer_logo_box">
                <div class="box_logo_l">
                  <span class="footer_logo">税</span>
                </div>
                <div class="box_logo_r">
                  <span class="zmbz">税费</span>
                  <div>100%税费透明</div>
                </div>
              </div>
            </li>
            <li>
              <div class="footer_logo_box">
                <div class="box_logo_l">
                  <span class="footer_logo">价</span>
                </div>
                <div class="box_logo_r">
                  <span class="zmbz">价格</span>
                  <div>价格适中</div>
                </div>
              </div>
            </li>
            <li>
              <div class="footer_logo_box">
                <div class="box_logo_l">
                  <span class="footer_logo">物</span>
                </div>
                <div class="box_logo_r">
                  <span class="zmbz">物流</span>
                  <div>物流便捷</div>
                </div>
              </div>
            </li>
            <li>
              <div class="footer_logo_box">
                <div class="box_logo_l">
                  <span class="footer_logo">售</span>
                </div>
                <div class="box_logo_r">
                  <span class="zmbz">售后</span>
                  <div>保证交易安全</div>
                </div>
              </div>
            </li>
          </ul>

          <div class="footer_detail">
              <ul>
                <li>
                  <div class="detail_title">
                    <span>购物指南</span>
                  </div>
                  <div class="detail_b">
                    <span>购物流程</span>
                    <span>发票制度</span>
                    <span>账户管理</span>
                  </div>
                </li>
                <li>
                  <div class="detail_title">
                    <span>支付方式</span>
                  </div>
                  <div class="detail_b">
                    <span>货到付款</span>
                    <span>在线支付</span>
                  </div>
                </li>
                <li>
                  <div class="detail_title">
                    <span>订单服务</span>
                  </div>
                  <div class="detail_b">
                    <span>订单状态说明</span>
                    <span>自动取消订单</span>
                  </div>
                </li>
                <li>
                  <div class="detail_title">
                    <span>配送方式</span>
                  </div>
                  <div class="detail_b">
                    <span>配送范围及免邮标准</span>
                    <span>验货签收</span>
                  </div>
                </li>
                <li>
                  <div class="detail_title">
                    <span>常见问题</span>
                  </div>
                  <div class="detail_b">
                    <span>常见问题整理汇集</span>
                    <span>投诉与监督</span>
                    <span>发票问题</span>
                  </div>
                </li>
              </ul>
          </div>
          <div class="footer_phone">
            <div class="footer_phone_b">
              <span class="phone_detail">400-829-8366</span>
              <span>周一至周日 8:00-18:00</span>
              <span>全国统一服务热线</span>
            </div>
          </div>
        </div>
      </div>
      <div class="footer_bootom">
        <div class="container">
          <div class="footer_bootom_img">
            <img src="../static/img/tubiao.png" alt="">
          </div>
          <div class="footer_bootom_t">
            <span>版权所有:</span>
            <span>西安国际陆港电子商贸有限公司</span>
          </div>
          <div class="footer_bootom_t2">
            <span>陕ICP备:</span>
            <span>15013404号</span>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style scoped>
.container-fluid{
  height: 370px;
  margin-top: 20px;
  border-top: 2px solid #EB193E;
}
  .footer_content ul {
    width: 100%;
    height: 160px;

  }
  .footer_content ul li{
    width: 234px;
    height: 160px;
    float: left;
  }
  .footer_logo_box{
    width: 170px;
    height: 65px;
    margin: 47px auto;
  }
  .box_logo_l {
    width: 63px;
    height: 65px;
    float: left;
  }
  .box_logo_r{
    width: 100px;
    height: 40px;
    margin-top: 12px;
    margin-left: 5px;
    float: left;
    font-size: 14px;
  }
  .box_logo_r span{
    font-weight: bold;
  }

  .footer_content .footer_logo{
    display: inline-block;
    width: 65px;
    height: 65px;
    font-size: 35px;
    color: #EB193E;
    text-align: center;
    background: url("../static/img/icon.png")no-repeat 0 -59px;
  }
  .footer_detail{
    width: 930px;
    height: 160px;
    float: left;
    font-size: 14px;

  }
  .footer_detail ul{
    display: flex;
    justify-content: space-between;
  }
  .footer_detail ul li{
    width:150px;
    height: 160px;
    float: left;

  }
  .detail_title{
    width:150px;
    height: 40px;
    line-height: 40px;
    font-size: 14px;
    font-weight: bold;
  }
  .detail_b span{
    width: 150px;
    height: 30px;
    line-height: 30px;
    font-size: 12px;
    display: block;
  }
  .footer_phone{
    width: 240px;
    height: 160px;
    float: left;
    border-left: 1px solid #ddd;
  }
  .footer_phone_b{
    width: 100%;
    height: 100px;
    margin-top: 20px;
  }
  .footer_phone span{
    text-align: center;
    display: block;
  }
  .phone_detail{
    font-size: 28px;
    font-weight: normal;
  }
  .footer_bootom{
    width: 100%;
    height: 50px;
    background: #343434;
  }
  .footer_bootom_img{
    width: 200px;
    height: 50px;
    float: left;
  }
  .footer_bootom img{
    margin-top: 10px;
  }
  .footer_bootom_t{
    width: 280px;
    height: 50px;
    line-height: 50px;
    float: left;
    font-size: 14px;
    color: white;
  }
  .footer_bootom_t2{
    float: left;
    width: 300px;
    height: 50px;
    line-height: 50px;
    font-size: 14px;
    color: white;
  }
</style>
