<template>
  <!-- <Greet name="Sanaz" role="developer" />
  <Greet name="Queena" role="talent acquisition" />
  <Greet name="Marina" role="marketing specialist" />
  <Greet :name="name" :role="role" /> -->

  <Article title="Article Title" :likes="5" :isPublished="true" />
</template>

<script>
import Greet from "./components/Greet.vue";
import Article from "./components/Article.vue";

export default {
  name: "App",
  components: {
    Greet,
    Article,
  },
  data() {
    return {
      name: "Fredrik",
      role: "CEO",
    };
  },
};
</script>

<style scoped></style>
