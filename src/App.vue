<template>
  <Greet name="Sanaz" role="developer" />
  <Greet name="Queena" role="talent acquisition" />
  <Greet name="Marina" role="marketing specialist" />
  <Greet :name="name" :role="role" />
</template>

<script>
import Greet from "./components/Greet.vue";
export default {
  name: "App",
  components: {
    Greet,
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
