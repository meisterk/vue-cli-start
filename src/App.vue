<template>
  <img alt="Logo der GBS Schulen München" src="./assets/logo.png" />
  <MyComponent ueberschrift="Hallo!" />
  <div class="zaehlercontainer">
    <MyCounter class="zaehler" ueberschrift="Zähler 1" @gezaehlt="gezaehlt1" />
    <MyCounter class="zaehler" ueberschrift="Zähler 2" @gezaehlt="gezaehlt2" />
    <MyCounter class="zaehler" ueberschrift="Zähler 3" @gezaehlt="gezaehlt3" />
  </div>
  <p class="gesamt">Gesamtzahl: {{ gesamtzahl }}</p>
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
      zahl3: 0,
    };
  },
  computed: {
    gesamtzahl() {
      return this.zahl1 + this.zahl2 + this.zahl3;
    },
  },
  methods: {
    gezaehlt1(zahl) {
      this.zahl1 = zahl;
    },
    gezaehlt2(zahl) {
      this.zahl2 = zahl;
    },
    gezaehlt3(zahl) {
      this.zahl3 = zahl;
    },
  },
};
</script>

<style>
.gesamt {
  background-color: yellowgreen;
  padding: 1em;
  margin: 0;
  text-align: center;
  border: 1px solid black;
}
.zaehlercontainer {
  display: flex;
}
.zaehler {
  flex: 1;
}
</style>
