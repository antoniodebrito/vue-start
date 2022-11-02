<template>
  <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default {
  name: "LifeCycle", 
  data() {
    return {
      nome: "Ninguém"
    }
  },
  created() {
    setTimeout(() => {
      this.nome = "Luis"
    }, 1000);

    this.lifeCycle()
  },
  mounted() {
    setTimeout(() => {
      this.nome = "Ricardo"
    }, 2000);
    this.lifeCycle()

  },
  methods: {
    lifeCycle() {
      console.log('Executou');
    }
  } 
}
</script>
