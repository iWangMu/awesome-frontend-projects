<script>
  import ShowTime from '../base/ShowTime.vue';
  export default {
    components: {
      ShowTime,
    },
  };
</script>
<template>
  <header>
    <h1>数据可视化-ECharts</h1>
    <ShowTime></ShowTime>
  </header>
</template>
<style scoped>
  header {
    background: url(../../static/images/head_bg.png) no-repeat top center;
    background-size: 100% 100%;
    height: 100px;
    color: #ffffff;
  }
  h1 {
    font-size: 38px;
    color: #ffffff;
    text-align: center;
    line-height: 80px;
  }
</style>
