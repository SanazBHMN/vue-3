<script>
export default {
  name: "App",
  data() {
    return {
      greet: "Hello",
      name: "Sanaz",
      location: "<b>Helsinki, Finland</b>",
      hack: `<a href='#' onclick='alert("You have been hacked!")'>Win a prize!</a>`,
    };
  },
};
</script>

<template>
  <p>{{ greet }} {{ name }}</p>
  <div v-html="location"></div>
  <div v-html="hack"></div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
