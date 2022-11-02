<template>
  <p>{{email}}</p>
  <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
  <p v-else>Estou em busca de novas oportunidades</p>
  <br>
  <p>Utilizo as seguintes tecnologias para back-end</p>
  <ul>
    <li  v-for="(thecnology, index) in backend_technologies" v-bind:key="index">
      {{ thecnology }}
    </li>
  </ul>
  
  <br><hr><br>

  <p>Utilizo as seguintes tecnologias para FrontEnd</p>
  <ul>
    <li v-for="thecnology in  frontend_technologies" :key="thecnology.id">
      {{thecnology.language}}
    </li>
  </ul>
  <br><br>
  <div>
    <button @click="showEmail">{{ textoBotao }}</button>
  </div>
  <p v-show="mostra_email">Mande uma mensagem para {{ email }}</p>
  <p class="teste">Para acessar meu portfólio basta <a v-bind:href="meu_link" target="_blank">clicar aqui</a></p>
  <Picture />
</template>

<script>
import Picture from './Picture.vue';

  export default {
    name: 'Info',
    components: {
      Picture 
    },
    props: {
      email: String,
      esta_trabalhando: Boolean,

    },
    data() {
      return {
        mostra_email: false,
        meu_link: "https://github.com/antoniodebrito",
        textoBotao: "Mostrar e-mail",
        backend_technologies: [
          'Ruby On Rails',
          'PHP',
          'Python',
          'Rust',
          'GoLang',
          'Node'
        ],
        frontend_technologies: [
          { id: 1, language: 'HTML' },
          { id: 2, language: 'CSS' },
          { id: 3, language: 'JavaScript' },
          { id: 4, language: 'Vue.js' },
          { id: 5, language: 'React.js' }
        ]
      }
    },
    methods: {
      showEmail() {
        this.mostra_email = !this.mostra_email
        if (!this.mostra_email) {
          this.textoBotao = "Mostrar e-mail"
        } else {
          this.textoBotao = 'Esconder e-mail'
        }
      }
    }
  }
</script>

<style>
  .paragrafo-pai {
    color: red;
  }
</style>