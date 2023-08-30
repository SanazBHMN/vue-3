<template>
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>
  <div v-for="actor in actors" :key="actor.name">
    <h2>{{ actor.name }}</h2>
    <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
  </div>
  <h2 v-for="(value, key, index) in myInfo" :key="value">
    {{ index }} {{ key }} {{ value }}
  </h2>

  <template v-for="name in names" :key="name">
    <h2>{{ name }}</h2>
    <hr />
  </template>

  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'Sanaz'">
      {{ name }}
    </h2>
  </template>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["Sanaz", "Queena", "Marina"],
      fullNames: [
        { first: "Sanaz", last: "Bahmani" },
        { first: "Queena", last: "Ahopalo" },
        { first: "Marina", last: "Makela" },
      ],
      actors: [
        {
          name: "Christian Bale",
          movies: ["Batman", "The Prestige"],
        },
        {
          name: "Di Caprio",
          movies: ["Titanic", "Inception"],
        },
      ],
      myInfo: {
        name: "Sanaz",
        age: 26,
        city: "Tehran",
      },
    };
  },
};
</script>

<style scoped></style>
