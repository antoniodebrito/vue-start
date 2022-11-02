<template>
    <h1>Ola mundo</h1>
    <p>Meu nome é {{nome}} e sou {{profissao}}</p>
    <MultiplosEventos />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
</template>

<script>
  import MultiplosEventos from './MultiplosEventos.vue'
  import Reutilizacao from './Reutilizacao.vue'

  export default {
    name: "PrimeiroComponente", 
    data(){
      return {
        nome: "Antonio",
        profissao: "programador"
      }
    },
    components: {
      MultiplosEventos,
      Reutilizacao
    }
  }
</script>