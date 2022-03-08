<template>
  <div v-for="(name, idx) in names" :key="idx">
    <h2 v-if="name.length >= 4">{{ name }}</h2>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      names: ["Don", "Harvey", "Jedi"],
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

ul {
  padding: 0;
}

li {
  list-style-type: none;
}
</style>
