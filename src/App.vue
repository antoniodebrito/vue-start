<template>
  <Header />
  <PrimeiroComponente />
  <p class="paragrafo-pai">O dado de app é {{testando}}</p>
  <LifeCycle />
  <Pessoa />
</template>

<script>
  import Header  from "./components/Header.vue";
  import PrimeiroComponente from './components/PrimeiroComponente.vue';
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue';

  export default {
    name: "App",
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa,
      Header
    },
    data() {
      return {
        testando: "Teste"
      }
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    background: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .teste {
    background: #000;
  }
</style>