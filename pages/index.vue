<template>
  <v-container class="pa-16">
    <v-row>
      <v-col cols="12" sm="3" class="d-flex justify-center aligm-center pa-4">
        <img src="https://github.com/felipeazsantos.png" width="150" class="perfil-image" />
      </v-col>
      <v-col cols="12" sm="9" class="d-flex align-center">
        Profissional com 5 anos de experiência em desenvolvimento de software.
        Atuei com tecnologias back-end e front-end.
        Estou sempre em busca de me desenvolver como profissional, estudando e aplicando tudo que aprendo.
      </v-col>
    </v-row>
    <v-row>
      <v-col xs="12">
        <Technologies />
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import Technologies from '@/components/home/Technologies.vue'

export default {
  name: 'IndexPage',
  components: { Technologies },
  head() {
    return {
      title: 'Felipe Azevedo dos Santos - Portfólio'
    }
  },
  
}
</script>

<style>
  .perfil-image {
    border-radius: 100%;
  }
</style>