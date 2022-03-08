<template>
  <div>
    <p v-if="num === 0">The number is {{ num }}</p>
    <p v-else-if="num < 0">Negative number: {{ num }}</p>
    <p v-else>Positive number: {{ num }}</p>
    <p v-show="show">Using v-show</p>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      num: 0,
      show: true
    }
  },
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
