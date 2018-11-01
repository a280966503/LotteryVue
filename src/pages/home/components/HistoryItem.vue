<template>
  <div class="item row" >
    <!--左边11个格子-->
    <div class="col-xs-11" >
      <!--开奖日期-->
      <div class="row  item-left">
        <span style="font-size: 18px;">第{{item.code}}期</span>
        <span style="margin-left: 10px;">{{item.date}}</span>
      </div>
      <!--开奖号码-->
      <div class="row item-left" style="margin-top: 10px;">
        <div class="ball-item ball-red" v-for="red in item.red.split(',')">{{red}}</div>

        <div class="ball-item ball-blue">{{item.blue}}</div>
      </div>
    </div>
    <!--右边1个格子-->
    <div class="col-xs-1 div-right" >
      <span class="glyphicon glyphicon-chevron-right"></span>
    </div>
  </div>

</template>

<script>
    export default {
        name: "HistoryItem",
      props:['item']
    }
</script>

<style scoped>
  .item{
    border: 1px solid gainsboro;height: 80px;padding-top: 5px;

  }
  .item-left {
    margin-left: 5px;
  }
  .div-right{
    padding-left: 0px;padding-top: 30px;
  }
</style>
