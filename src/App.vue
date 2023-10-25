<template>
  <h2>{{ name }}</h2>
  <div>
    <button v-on:mouseover="name = 'Queena'">Change Name</button>
  </div>

  <div>
    <p>event object</p>
    <button @click="changeName($event), increment(1, $event)">
      Change Name
    </button>
  </div>

  <h2>{{ count }}</h2>
  <p>Inline event handling</p>
  <button @click="count += 1">Incremant</button>
  <button @click="count -= 1">Decrement</button>

  <p>Define methods</p>
  <button @click="increment(1, $event)">Increment 1</button>
  <button @click="increment(5)">Increment 5</button>
  <button @click="decrement(1)">Decrement 1</button>
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
    changeName(event) {
      this.name = "Queena";
      console.log(event);
    },
    increment(num, event) {
      this.count += num;
      console.log(event);
    },
    decrement(num) {
      this.count -= num;
    },
  },
};
</script>

<style scoped></style>
