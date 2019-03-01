<template>
  <div id="app">
    <div id="nav-header">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand" href="#">
          <img src="./assets/ruths_ai.png" width="100" height="50" class="d-inline-block align-top" alt="">
        </a>
        <!--align like a actual nav bar-->
        <div class="navbar-nav">
          <a
            v-for="comp in comps"
            v-bind:key="comp"
            v-bind:class="['nav-item nav-link', {active: curComp === comp}]"
            v-on:click="curComp = comp">
            {{comp}}
          </a>
        </div>
      </nav>
    </div>
    <div class="pages">
    <page
    v-bind:is="curPageComp"
    v-bind:msg=curComp
    class="comp">
    </page>
    </div>
  </div>
</template>

<script>
import Intro from './components/Intro.vue'
import Data from './components/Data.vue'

export default {
  name: 'app',
  components: {
    Intro,
    Data
  },
  data: function() {
    return {
      curComp: 'Intro',
      comps: ['Intro', 'Data']
    }
    
  },
  computed: {
    curPageComp: function() {
      return this.curComp;
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #000000;
}
</style>
