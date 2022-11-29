<template>
  <Header :esta_logado="true" />
  <PrimeiroComponente />
  <p class="paragrafo-pai">Hey there!</p>
  <LifeCycle />
  <Pessoa/>
</template>

<script>
import Header from "./components/Header.vue";
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
import LifeCycle from "./components/LifeCycle.vue"
import Pessoa from "./components/Pessoa.vue"

export default {
  name: "App",
  components: {
    Header,
    PrimeiroComponente,
    LifeCycle,
    Pessoa
  },
};
</script>

<style>
  body {
    background-color: #333;
    color: #FFF;
  }

  a {
    color: #000;
  }

  .teste {
    background-color: #555;
  }
</style>