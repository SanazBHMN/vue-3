<template>
  <h2>Hello! {{ name }}: {{ role }}</h2>
</template>

<script>
export default {
  name: "Greet",
  props: ["name", "role"],
};
</script>
