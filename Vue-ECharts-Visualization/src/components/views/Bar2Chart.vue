<script>
  import * as echarts from 'echarts';
  export default {
    data() {
      return {
        barColors: ['#1089E7', '#F57474', '#56D0E3', '#F8B448', '#8B78F6'],
      };
    },
    mounted() {
      const myChart = echarts.init(document.querySelector('.bar2chart'));
      const colors = this.barColors;
      const options = {
        grid: {
          top: '10%',
          left: '22%',
          bottom: '10%',
          containLabel: false,
        },
        xAxis: {
          show: false,
        },
        yAxis: [
          {
            axisLine: {
              show: false,
            },
            axisTick: {
              show: false,
            },
            axisLabel: {
              color: '#ffffff',
            },
            type: 'category',
            inverse: true,
            data: ['HTML5', 'CSS3', 'JavaScript', 'Vue3', 'Node'],
          },
          {
            show: true,
            inverse: true,
            data: [702, 342, 601, 783, 694],
            axisLine: {
              show: false,
            },
            axisTick: {
              show: false,
            },
            axisLabel: {
              textStyle: {
                fontSize: 12,
                color: '#ffffff',
              },
            },
          },
        ],
        series: [
          {
            name: '条',
            type: 'bar',
            barCategoryGap: 50,
            barWidth: 10,
            itemStyle: {
              barBorderRadius: 20,
              color: function (params) {
                return colors[params.dataIndex % colors.length];
              },
            },
            label: {
              show: true,
              color: '#ffffff',
              fontSize: 10,
              verticalAlign: 'middle',
              position: 'inside',
              formatter: '{c}%',
            },
            yAxisIndex: 0,
            data: [70, 34, 60, 78, 69],
          },
          {
            name: '框',
            type: 'bar',
            barCategoryGap: 50,
            barWidth: 15,
            itemStyle: {
              color: 'none',
              borderColor: '#00c1de',
              borderWidth: 3,
              barBorderRadius: 15,
            },
            yAxisIndex: 1,
            data: [100, 100, 100, 100, 100],
          },
        ],
      };
      myChart.setOption(options);
      window.addEventListener('resize', () => myChart.resize());
    },
  };
</script>
<template>
  <h2>柱状图-技能掌握</h2>
  <div class="bar2chart"></div>
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
  .bar2chart {
    width: 100%;
    height: 240px;
  }
</style>
