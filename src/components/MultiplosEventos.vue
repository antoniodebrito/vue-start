<template>
  <div>
    <input type="text" v-model="txt">
    <button 
      @click="
      primeiro(txt, $event), 
      segundo($event),
      terceiro($event)
    ">
      Ativar multiplos eventos
    </button>
    <p>Digite seu nome {{multiplos_eventos}}</p>
  </div>
</template>

<script>
  export default {
    name: 'MultiplosEventos',
    data() {
      return {
        multiplos_eventos: ''
      }
    },
    methods: {
      primeiro(txt,e) {
        this.multiplos_eventos = txt
      },
      segundo(e) {
        setTimeout(() => {
          this.multiplos_eventos = "Registrado com sucesso"
        }, 1000);
      },
      terceiro(e) {
        setTimeout(() => {
          this.multiplos_eventos = ""
        }, 1500);
      }
    }
  }
</script>

<style scoped>
  div {
    margin: 100px;
  }
</style>