<template>
  <img alt="Logo der GBS Schulen München" src="./assets/logo.png" />
  <MyComponent ueberschrift="Hallo!" />
  <MyForm />
  <MyComponent ueberschrift="Servus!" />
</template>

<script>
import MyComponent from "./components/MyComponent.vue";
import MyForm from "./components/MyForm.vue";

export default {
  name: "App",
  components: {
    MyComponent,
    MyForm,
  },
};
</script>

<style>
</style>
