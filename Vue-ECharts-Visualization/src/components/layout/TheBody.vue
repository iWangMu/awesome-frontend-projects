<script>
  import ChartCard from '../base/ChartCard.vue';
  import BarChart from '../views/BarChart.vue';
  import Bar2Chart from '@/components/views/Bar2Chart.vue';
  import Line1Chart from '@/components/views/Line1Chart.vue';
  import NumberChart from '@/components/views/NumberChart.vue';
  import MapChart from '@/components/views/MapChart.vue';
  export default {
    components: {
      ChartCard,
      BarChart,
      Bar2Chart,
      Line1Chart,
      NumberChart,
      MapChart,
    },
  };
</script>
<template>
  <section>
    <div class="chartsView">
      <ChartCard><BarChart></BarChart></ChartCard>
      <ChartCard><Line1Chart></Line1Chart></ChartCard>
      <ChartCard></ChartCard>
    </div>
    <div class="chartsView">
      <NumberChart></NumberChart>
      <MapChart></MapChart>
    </div>
    <div class="chartsView">
      <ChartCard><Bar2Chart></Bar2Chart></ChartCard>
      <ChartCard></ChartCard>
      <ChartCard></ChartCard>
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
    margin: 0 10px;
  }
</style>
