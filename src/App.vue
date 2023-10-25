<template>
  <h2>{{ name }}</h2>
  <div>
    <button v-on:mouseover="name = 'Queena'">Change Name</button>
  </div>

  <h2>{{ count }}</h2>
  <p>Inline event handling</p>
  <button v-on:click="count += 1">Incremant</button>
  <button v-on:click="count -= 1">Decrement</button>

  <p>Define methods</p>
  <button v-on:click="increment(1)">Increment 1</button>
  <button v-on:click="increment(5)">Increment 5</button>
  <button v-on:click="decrement(1)">Decrement 1</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Sanaz",
      count: 0,
    };
  },
  methods: {
    increment(num) {
      this.count += num;
    },
    decrement(num) {
      this.count -= num;
    },
  },
};
</script>

<style scoped></style>
