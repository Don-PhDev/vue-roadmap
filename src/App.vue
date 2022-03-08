<template>
  <div>
    <h1>{{ greet }} {{ name }}</h1>
    <p v-html="language" />
    <h3 :id="headingId">Heading</h3>
    <button :disabled="isDisabled">Click me</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      greet: "Hello",
      name: "Don",
      language: "<b>Vue JS</b>",
      headingId: "heading",
      isDisabled: true,
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
