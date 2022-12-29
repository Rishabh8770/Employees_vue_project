<template>
  <div id="app">
    <Employees/>
  </div>
</template>
<script>
  import Employees from './components/Employees.vue'
  export default {
    name: 'App',
    components: {
      Employees
    }
  }
</script>

<style>
 #app {
  padding: 20px;
  width: 100%;
  text-align: center;
 }
</style>