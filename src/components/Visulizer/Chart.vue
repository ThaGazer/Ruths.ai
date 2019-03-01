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
          text: 'Well Data'
        },
        tooltip: {},
        legend: {
        },
        xAxis: {
          data: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
        },
        yAxis: {},
        series: [
          {
            name: 'Oil Rate',
            type: 'line',
            data: [0.73, 1.02, 0.2, 0.56, 0, 0, 0.04, 0.27, 0.59, 0.26, 0.52, 0.89]
          },
          {
            name: 'Gas Rate',
            type: 'line',
            data: [17.42, 39.64, 14.91, 25.27, 68.27, 3.07, 12.75, 33.96, 16.26, 11.98, 17.14, 36.8]
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