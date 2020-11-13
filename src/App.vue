<template>
  <img alt="Logo der GBS Schulen München" src="./assets/logo.png" />
  <MyComponent ueberschrift="Hallo!" />
  <MyComponent ueberschrift="Servus!" />
  <MyComponent ueberschrift="Griasde!" />
</template>

<script>
import MyComponent from "./components/MyComponent.vue";

export default {
  name: "App",
  components: {
    MyComponent,
  },
};
</script>

<style>
</style>
