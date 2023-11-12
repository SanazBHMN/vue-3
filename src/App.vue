<template>
  <!-- <Greet name="Sanaz" role="developer" />
  <Greet name="Queena" role="talent acquisition" />
  <Greet name="Marina" role="marketing specialist" />
  <Greet :name="name" :role="role" /> -->

  <Article
    id="my-article"
    title="Article Title"
    :likes="5"
    :isPublished="true"
  />

  <br />

  <h2>App component username: {{ name }}</h2>
  <ComponentC />
</template>

<script>
import Greet from "./components/Greet.vue";
import Article from "./components/Article.vue";
import ComponentC from "./components/ComponentC.vue";

export default {
  name: "App",
  components: {
    Greet,
    Article,
    ComponentC,
  },
  data() {
    return {
      name: "Fredrik",
      role: "CEO",
    };
  },
  provide() {
    return {
      username: this.name,
    };
  },
};
</script>

<style scoped></style>
