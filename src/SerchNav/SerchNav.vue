<template>
    <div class="Serch_nav container-fluid">
      <div class="container" style="height: 130px;">
        <SerchLeft class="serchleft "></SerchLeft>
        <SerchRight class="serchright "></SerchRight>
      </div>
    </div>
</template>

<script>
  import SerchLeft from './component/SerchLeft'
  import SerchRight from './component/SerchRight'
    export default {
        name: "SerchNav",
      components:{
        SerchLeft,
        SerchRight
      }

    }
</script>

<style scoped lang="less">
  @import "../static/css/common.less";
  .Serch_nav{
    height: 130px;
  }
  .serchleft{
    width: 30%;
    float: left;
  }
  .serchright{
    width: 69%;
    float: left;
  }
</style>
