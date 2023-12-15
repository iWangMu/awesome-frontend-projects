<script>
  import ChartCard from '../base/ChartCard.vue';
  import BarChart from '../views/BarChart.vue';
  export default {
    components: {
      ChartCard,
      BarChart,
    },
  };
</script>
<template>
  <section>
    <div class="chartsView">
      <ChartCard><BarChart></BarChart></ChartCard>
      <ChartCard><BarChart></BarChart></ChartCard>
      <ChartCard><BarChart></BarChart></ChartCard>
    </div>
    <div class="chartsView">456</div>
    <div class="chartsView">
      <ChartCard><BarChart></BarChart></ChartCard>
      <ChartCard><BarChart></BarChart></ChartCard>
      <ChartCard><BarChart></BarChart></ChartCard>
    </div>
  </section>
</template>
<style scoped>
  section {
    display: flex;
    margin-top: 5px;
    padding: 10px;
  }
  .chartsView {
    flex: 3;
  }
  .chartsView:nth-child(2) {
    flex: 5;
  }
</style>
