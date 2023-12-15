<script>
  import * as echarts from 'echarts';

  export default {
    data() {},
    mounted() {
      const myChart = echarts.init(document.querySelector('.chart'));
      const options = {
        xAxis: {
          type: 'category',
          data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
        },
        yAxis: {
          type: 'value',
        },
        series: [
          {
            data: [120, 200, 150, 80, 70, 110, 130],
            type: 'bar',
          },
        ],
      };
      myChart.setOption(options);
    },
  };
</script>
<template>
  <h2>柱状图-就业行业</h2>
  <div class="chart"></div>
</template>

<style scoped>
  h2 {
    height: 40px;
    line-height: 40px;
    text-align: center;
    font-size: 16px;
    font-weight: 500;
    color: #ffffff;
  }
  .chart {
    width: 100%;
    height: 240px;
  }
</style>
