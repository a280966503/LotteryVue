<template>
    <div class="row title">
      <div class="col-xs-12">
        <div class="div-back" v-if="needback">&lt;返回</div>
      </div>
      {{title}}
    </div>
</template>

<script>


    export default {
        name: "TitleBar",
      props:['title','needback']

    }
</script>

<style scoped>
  .div-back{
    position: absolute;
  }
</style>
