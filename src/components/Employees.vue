<template>
  <div>
    <h1 id="header">Employee Table</h1>
    <table border="1px" width="100%">
      <tr>
        <td>Name</td>
        <td>salary</td>
        <td>Age</td>
      </tr>
      <tr v-for="item in list" v-bind:key="item.id">
        <td>{{item.employee_name}}</td>
        <td>{{item.employee_salary}}</td>
        <td>{{item.employee_age}}</td>
      </tr>
    </table>
  </div>
</template>
<script>

import axios from 'axios'

export default {
  name: 'Employees',
  data()
  {
    return {list:undefined}
  },
  mounted () {
    console.log("Hello")
    axios
      .get('https://dummy.restapiexample.com/api/v1/employees')
      .then(res => {
        this.list = res.data.data;
        console.warn(res.data.data)
      })
  }
}
</script>
<style>
  #header {
    color: blue;
    border: 2px solid black;
    margin: 1rem;
  }
</style>
