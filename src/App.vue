<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>DATA ITER</h1>
    <data-iter/>
    <hr/>
    <br/>
    <simple-table/>
    <br/>
    <data-table/>
  </div>
</template>

<script>
import DataIter from './components/DataIter.vue';
import DataTable from './components/DataTable.vue';
import SimpleTable from './components/SimpleTable.vue';

export default {
  name: 'App',
  components: {
    SimpleTable,
    DataTable,
    DataIter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
