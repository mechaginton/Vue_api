<template>
  <div class='app'>
    <div>{{ displayValue }}</div>
    <div>
      <input type='text' v-model='inputValue'>
      <input type='text' v-model='inputPeriod'>
      <input type='text' v-model='inputDetail'>
    </div>
    <div>
      <button v-on:click='createTask'>追加</button>
    </div>
  </div>
</template>

<script>
import api from '../api/api'

export default {
  name: 'app',
  data () {
    return {
      inputValue: '',
      inputPeriod: '',
      inputDetail: ''
    }
  },
  methods: {
    async createTask () {
      const result = await api.post('/tasks', {
        title: this.inputValue,
        period: this.inputPeriod,
        detail: this.inputDetail
      })
      console.log(result)
    }
  }
}
</script>

<style>
.app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
