<template>
  <img :src="avatar" :alt="descricao">
  <MudarImage @mudar-imagem="trocarImage" />
</template>

<script>
  import MudarImage from './MudarImage.vue'

  export default {
    name: 'Picture',
    data() {
      return {
        avatar: "/img/avatar.png",
        descricao: "Antonio Brito"
      }
    },
    components: {
      MudarImage
    },
    methods: {
      trocarImage() {
        this.avatar = '/img/avatar-2.png'
      }
    }
  }
</script>