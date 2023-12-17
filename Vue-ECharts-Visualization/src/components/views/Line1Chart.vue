<script>
  import * as echarts from 'echarts';
  export default {
    mounted() {
      const myChart = echarts.init(document.querySelector('.linechart'));
      const options = {
        color: ['#00f2f1', '#ed3f35'],
        tooltip: {
          trigger: 'axis',
        },
        legend: {
          textStyle: {
            color: '#4c9bfd',
          },
          right: '10%',
        },
        grid: {
          top: '20%',
          left: '3%',
          right: '4%',
          bottom: '3%',
          show: true,
          borderColor: '#012f4a',
          containLabel: true,
        },
        xAxis: {
          type: 'category',
          data: ['1月', '2月', '3月', '4月', '5月', '6月', '7月', '8月', '9月', '10月', '11月', '12月'],
          axisTick: {
            show: false,
          },
          axisLabel: {
            color: '#4c9bfd',
          },
          axisLine: {
            show: false,
          },
          boundaryGap: false,
        },
        yAxis: {
          type: 'value',
          axisTick: {
            show: false,
          },
          axisLabel: {
            color: '#4c9bfd',
          },
          axisLine: {
            show: false,
          },
          splitLine: {
            lineStyle: { color: '#012f4a' },
          },
        },
        series: [
          {
            name: '新增粉丝',
            type: 'line',
            data: [24, 40, 101, 134, 90, 230, 210, 230, 120, 230, 210, 120],
            smooth: true,
          },
          {
            name: '新增游客',
            type: 'line',
            data: [40, 64, 191, 324, 290, 330, 310, 213, 180, 200, 180, 79],
            smooth: true,
          },
        ],
      };
      myChart.setOption(options);
      window.addEventListener('resize', () => myChart.resize());
    },
  };
</script>
<template>
  <h2>折线图-人员变化</h2>
  <div class="linechart"></div>
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
  .linechart {
    width: 100%;
    height: 240px;
  }
</style>
