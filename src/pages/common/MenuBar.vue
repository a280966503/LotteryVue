<template>
    <div class="div-height">
      <!--5.底部菜单栏-->
      <div class="menu">
        <div class="col-xs-4 menu-item " :class="{'menu-item-activied':index=='1'}">
          <span class="glyphicon glyphicon-home"></span>
          <p>首页</p>
        </div>
        <div class="col-xs-4 menu-item" :class="{'menu-item-activied':index=='2'}">
          <span class="glyphicon glyphicon-shopping-cart"></span>
          <p>选号</p>
        </div>
        <div class="col-xs-4 menu-item" :class="{'menu-item-activied':index=='3'}">
          <span class="glyphicon glyphicon-user"></span>
          <p>我</p>
        </div>

      </div>
    </div>
</template>

<script>
    export default {
        name: "MenuBar",
      props:{
          index:{
            type:String,
            default:'1'
          }
      }
    }
</script>

<style scoped>
.div-height{
  height: 50px;
}
</style>
