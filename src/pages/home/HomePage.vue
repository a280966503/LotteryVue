<template>
  <div>
    <title-bar :title="title" ></title-bar>

    <carousel></carousel>

    <history-list :data="historyList"></history-list>

    <menu-bar index="1"></menu-bar>
  </div>
</template>

<script>

  import TitleBar from '@/pages/common/TitleBar'
  import Carousel from '@/pages/common/Carousel'
  import HistoryList from '@/pages/home/components/HistoryList'
  import MenuBar from '@/pages/common/MenuBar'
  import axios from 'axios'


  export default {
    name: "HomePage",
    data() {
      return{
        title:'博彩首页',
        needback:'true',
        historyList:[]
      }
    },
    components: {
      TitleBar,
      Carousel,
      HistoryList,
      MenuBar
    },
    mounted(){
      axios.get('/api/index').then(res=>{
        this.historyList=res.data.data
      })
    }
  }
</script>

<style scoped>

</style>
