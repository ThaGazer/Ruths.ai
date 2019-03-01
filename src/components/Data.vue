<template>
  <div id="data">
    <div class="jumbotron jumbotron-fluid bg-black text-color-white">
      <div class="container">
        <h1 class="display-4">Data</h1> 
      </div>  
    </div>
    <div class="components">
        <div class="comp1">
            <WellPicker/>
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

export default {
    name: "Data",
    components: {
        WellPicker,
        Chart
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
</style>

