<template>
  <!-- <Greet name="Sanaz" role="developer" />
  <Greet name="Queena" role="talent acquisition" />
  <Greet name="Marina" role="marketing specialist" />
  <Greet :name="name" :role="role" /> -->

  <!-- <Article
    id="my-article"
    title="Article Title"
    :likes="5"
    :isPublished="true"
  /> -->

  <!-- <br /> -->

  <!-- <h2>App component username: {{ name }}</h2>
  <ComponentC /> -->
  <button @click="showPopup = true">Show Popup</button>
  <Popup v-show="showPopup" @close="closePopup" />
</template>

<script>
import Greet from "./components/Greet.vue";
import Article from "./components/Article.vue";
import ComponentC from "./components/ComponentC.vue";
import Popup from "./components/Popup.vue";

export default {
  name: "App",
  components: {
    Greet,
    Article,
    ComponentC,
    Popup,
  },
  data() {
    return {
      name: "Fredrik",
      role: "CEO",
      showPopup: false,
    };
  },
  methods: {
    closePopup(name) {
      this.showPopup = false;
      console.log("Name: ", name);
    },
  },
  provide() {
    return {
      username: this.name,
    };
  },
};
</script>

<style scoped></style>
