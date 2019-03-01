<template>
  <div class="echarts">
    <IEcharts
      :option="bar"
    />
  </div>
</template>

<script type="text/babel">
  import IEcharts from 'vue-echarts-v3/src/full.js';
  export default {
    name: 'view',
    components: {
      IEcharts
    },
    props: [
      'showTheseWells',
      'wells'
    ],
    data: () => ({
      bar: {
        title: {
          text: 'ECharts Hello World'
        },
        tooltip: {},
        xAxis: {
          data: ['Shirt', 'Sweater', 'Chiffon Shirt', 'Pants', 'High Heels', 'Socks']
        },
        yAxis: {},
        series: [
          {
            name: 'Sales',
            type: 'line',
            data: [5, 20, 36, 10, 10, 20]
          },
          {
            name: 'Saless',
            type: 'line',
            data: [10, 4, 15, 20, 30, 20]
          }
        ]
      }
    }),
    methods: {
      doRandom() {        
        let data = [];
        for (let i = 0, min = 5, max = 99; i < 6; i++) {
          data.push(Math.floor(Math.random() * (max + 1 - min) + min));
        }
        this.bar.series[0].data = data;
      },
    }
  };
</script>

<style scoped>
  .echarts {
    width: 800px;
    height: 400px;
  }
</style>