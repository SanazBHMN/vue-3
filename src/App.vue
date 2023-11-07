<template>
  <h2>Volume Tracker (0-20)</h2>
  <h3>Current Volume - {{ volume }}</h3>
  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      volume: 0,
    };
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      console.log("New Value: ", newValue);
      console.log("Old Value: ", oldValue);
      if (newValue === 16 && newValue > oldValue) {
        alert(
          "Listening to a high volume for a long time may damage your hearing!"
        );
      }
    },
  },
};
</script>

<style scoped></style>
