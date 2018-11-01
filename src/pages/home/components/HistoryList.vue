<template>
    <div>
      <history-item v-for="item in data" :item="item"></history-item>
    </div>
</template>

<script>
  import HistoryItem from './HistoryItem'

    export default {
        name: "HistoryList",
      components:{
          HistoryItem
      },
      props:['data']
    }
</script>

<style scoped>

</style>
