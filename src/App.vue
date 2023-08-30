<script>
export default {
  name: "App",
  data() {
    return {
      num: "Hi",
      display: true,
      showElement: false,
    };
  },
};
</script>

<template>
  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else>Not a number</h2>

  <template v-if="display">
    <h2>Sanaz</h2>
    <h2>Software Developer</h2>
    <h2>JobGo International Oy</h2>
  </template>

  <h2 v-show="showElement">Using v-show</h2>
  <h2 v-if="showElement">Using v-if</h2>
</template>

<style scoped></style>
