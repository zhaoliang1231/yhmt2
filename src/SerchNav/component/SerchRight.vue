<template>
    <div>
      <div class="serchBox">
        <div class="" style="position: absolute;top: 30px;width: 100%">
          <div class="serch_top">
            <input type="text"  name="" id="" placeholder="UGG  香奈儿">
            <img src="" alt="">
            <div class="sherch_bnt">搜索</div>
          </div>
          <div class="serch_tip">
            <span>香奈儿</span>
            <label>|</label>
            <span>奶粉</span>
            <label>|</label>
            <span>UGG</span>
            <label>|</label>
            <span>家居</span>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
        name: "SerchRight"
    }
</script>

<style scoped lang="less">
  @import "../../static/css/common";
 .serchBox{
   width: 100%;
   height: 130px;
   /*border: 1px solid saddlebrown;*/
   position: relative;
   .serch_top{
     /*width: 690px;*/
     /*border: 1px solid;*/
    height: 40px;
   }
   input{
     width: 50%;
     height: 40px;
     outline: none;
     border: 2px solid @redLightColor;
     float: left;
     font-size: 14px;
      padding-left: 10px;
   }
   .sherch_bnt{
     width: 80px;
     height: 40px;
     background: @redLightColor;
     float: left;
     text-align: center;
     line-height: 40px;
     color: white;
   }
   .serch_tip{
     font-size: 12px;
     color: @redFont;
     position: absolute;
     top: 45px;
     span{
       cursor: pointer;
     }
   }
 }


</style>
