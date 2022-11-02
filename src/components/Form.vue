<template>
  <form @submit="enviarFormulario($event)">
    <div>
      <input type="text" v-model="name">
    </div>
    <div>
      <input type="text" v-model="email">
    </div>
    <div><submit /></div>
  </form>
  <p>{{name}}</p>
  <p>{{email}}</p>
  <p>Formulario</p>

</template>

<script>
import Input from './Form/Input.vue'
import Submit from './Form/Submit.vue'

export default {
  name: 'Form',
  components: {
    Input,
    Submit
  },
  data() {
    return {
      name: '',
      email: ''
    }
  },
  methods: {
    enviarFormulario(e) {
      const name = this.name;
      const email = this.email;

      e.preventDefault();
      console.log(name, email);

      //inserir os dados no banco
    }
  }
}
</script>

<style scoped>
  p {
    padding: 150px;
  }
</style>