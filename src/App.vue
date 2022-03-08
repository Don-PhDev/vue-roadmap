<template>
  <div>
    <ul v-for="(name, i) in userNames" :key="i">
      <li>{{ name }}</li>
    </ul>
    <ul>
      <li v-for="(name, i) in fullNames" :key="i">{{ name.first }} {{ name.last }}</li>
    </ul>

    <div v-for="actor in actors" :key="actor.name">
      <h3>{{ actor.name }}</h3>
      <h4 v-for="(movie, i) in actor.movies" :key="i">{{ movie }}</h4>
    </div>
  </div>
  <h3 v-for="(val, k, i) in myInfo" :key="i">{{ k }} {{ val }} {{ i }}</h3>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      userNames: ["Don", "Harvey", "Jedi"],
      fullNames: [
        { first: "Bruce", last: "Wayne" },
        { first: "Mike", last: "Laycan" },
        { first: "Lisa", last: "Murray" },
      ],
      actors: [
        {
          name: "Christian Bale",
          movies: ["Batman", "The Prestige"]
        },
        {
          name: "Leonardo Di Caprio",
          movies: ["Titanic", "Inception", "Shutter Island"]
        }
      ],
      myInfo: {
        name: "Don Forrest",
        age: 17,
        language: "Filipino"
      }
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
