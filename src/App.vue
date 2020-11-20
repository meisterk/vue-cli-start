<template>
  <img alt="Logo der GBS Schulen München" src="./assets/logo.png" />
  <MyComponent ueberschrift="Hallo!" />
  <MyCounter ueberschrift="Zähler1" @gezaehlt="gezaehlt1" />
  <MyCounter ueberschrift="Zähler2" @gezaehlt="gezaehlt2" />
  <p>Gesamtzahl: {{ gesamtzahl }}</p>
  <MyForm />
  <MyComponent ueberschrift="Servus!" />
</template>

<script>
import MyComponent from "./components/MyComponent.vue";
import MyForm from "./components/MyForm.vue";
import MyCounter from "./components/MyCounter.vue";

export default {
  name: "App",
  components: {
    MyComponent,
    MyForm,
    MyCounter,
  },
  data() {
    return {
      zahl1: 0,
      zahl2: 0,
    };
  },
  computed: {
    gesamtzahl() {
      return this.zahl1 + this.zahl2;
    },
  },
  methods: {
    gezaehlt1(zahl) {
      this.zahl1 = zahl;
    },
    gezaehlt2(zahl) {
      this.zahl2 = zahl;
    },
  },
};
</script>

<style>
</style>
