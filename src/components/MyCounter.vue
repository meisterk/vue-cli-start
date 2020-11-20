<template>
  <div class="container">
    <h1>{{ ueberschrift }}</h1>
    <button @click="hochzaehlen">Hochzählen</button>
    <p>{{ zahl }}</p>
  </div>
</template>

<script>
export default {
  name: "MyCounter",
  props: {
    ueberschrift: String,
  },
  data() {
    return {
      zahl: 0,
    };
  },
  methods: {
    hochzaehlen() {
      this.zahl++;
      this.$emit("gezaehlt", this.zahl);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  background-color: yellow;
  border: 1px solid black;
  padding: 0.5em;
  text-align: center;
}
</style>
