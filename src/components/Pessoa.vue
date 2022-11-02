<template>
  <h2>Esta é a descrição da pessoa: </h2>
  <Info />
  <Form />
</template>


<script>
  import Form from './Form.vue'
  import Info from './Info.vue'
  export default {
    name: 'Pessoa',
    components: {
      Info,
      Form
    },
    data() {
      return {
        nome: "Matheus"
      }
    }
  }
</script>