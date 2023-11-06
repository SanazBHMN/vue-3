<template>
  <h2>Fullname: {{ firstName }} {{ lastName }}</h2>
  <h2>Computed fullname: {{ fullName }}</h2>

  <!-- <h2>
    Total: {{ items.reduce((total, curr) => (total = total + curr.price), 0) }}
  </h2> -->
  <button
    @click="
      items.push({
        id: 4,
        title: 'Keyboard',
        price: 50,
      })
    "
  >
    Add item
  </button>
  <h2>Computed total: {{ total }}</h2>

  <h2>Method Total: {{ getTotal() }}</h2>

  <input type="text" v-model="country" />
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firstName: "Sanaz",
      lastName: "Bahmani",
      items: [
        {
          id: 1,
          title: "TV",
          price: 100,
        },
        {
          id: 2,
          title: "Phone",
          price: 200,
        },
        {
          id: 3,
          title: "Laptop",
          price: 300,
        },
      ],
      country: "",
    };
  },
  methods: {
    getTotal() {
      console.log("getTotal method");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
  },
  computed: {
    fullName() {
      console.log("total computed property");
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
  },
};
</script>

<style scoped></style>
