<script>
  import * as echarts from 'echarts';

  export default {
    data() {},
    mounted() {
      const myChart = echarts.init(document.querySelector('.chart'));
      const options = {
        color: ['#2f89cf'],
        tooltip: {
          show: true,
          trigger: 'axis',
          axisPointer: {
            type: 'shadow',
          },
        },
        grid: {
          top: '10px',
          left: '0%',
          right: '0%',
          bottom: '4%',
          containLabel: true,
        },
        xAxis: {
          type: 'category',
          data: ['旅游行业', '教育培训', '游戏行业', '医疗行业', '电商行业', '社交行业', '金融行业'],
          axisLabel: {
            color: 'rgba(255, 255, 255, 0.6)',
            fontSize: '12px',
          },
          axisLine: {
            show: false,
          },
        },
        yAxis: {
          type: 'value',
          axisLabel: {
            color: 'rgba(255, 255, 255, 0.6)',
            fontSize: '12px',
          },
          axisLine: {
            show: true,
            lineStyle: {
              color: 'rgba(255, 255, 255, 0.1)',
              width: 1,
            },
          },
          splitLine: {
            lineStyle: {
              color: 'rgba(255, 255, 255, 1)',
            },
          },
        },
        series: [
          {
            data: [200, 300, 300, 900, 1500, 1200, 600],
            type: 'bar',
            barWidth: '35%',
            itemStyle: {
              borderRadius: 3,
            },
          },
        ],
      };
      myChart.setOption(options);
      window.addEventListener('resize', () => myChart.resize());
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
