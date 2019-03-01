<template>
  <div id="data">
    <div class="jumbotron jumbotron-fluid bg-black text-color-white">
      <div class="container">
        <h1 class="display-4">Data</h1> 
      </div>  
    </div>
    <div class="components">
        <div class="comp1">
            <div id="WellPicker" style="width: 280px; height: 1000px">
              <h1>Pick a Well</h1>
              <div class="list-group" id="list-tab" role="tablist">
                  <WellPicker
                    v-for="well in simplifiedWells()"
                    v-bind:key="well"
                    v-bind:title="well"
                  ></WellPicker>
              </div>
            </div>
        </div>    
        <div class="comp2">
            <Chart/>
        </div>
    </div>
  </div>
</template>

<script>
import Chart from './Visulizer/Chart.vue'
import WellPicker from './Visulizer/WellPicker.vue'
import apiCall from '../assets/api_response.json'

export default {
    name: "Data",
    components: {
        WellPicker,
        Chart
    },
    data: function() {
      return {
        wells: apiCall.data
      }
    },
    methods: {
      simplifiedWells() {
        let simpleWells = [];
        for(let i = 0; i < this.wells.length; i++) {
          if(!simpleWells.includes(this.wells[i].wellId)) {
            simpleWells.push(this.wells[i].wellId);
          }
        }
        return simpleWells;
      }
    }
}
</script>

<style scoped>
.bg-black {
  background-color: #000000;
}
.text-color-white {
  color: #ffffff;
}
.comp1 {
    float: left;
}
.comp2 {
    display:inline-block
}
.list-group {
  max-height: 1000px;
  overflow: scroll;
}
</style>

