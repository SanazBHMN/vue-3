<template>
  <h2>component C</h2>
  <componentE />
</template>

<script>
import ComponentE from "./ComponentE.vue";

export default {
  name: "ComponentC",
  components: {
    ComponentE,
  },
};
</script>

<style scoped></style>
