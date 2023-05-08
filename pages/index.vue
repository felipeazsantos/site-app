<template>
  <v-container class="pa-16">
    <v-row>
      <v-col>
        <h2 class="indigo--text text--darken-2 text-center">Sobre</h2>
      </v-col>
    </v-row>
    <v-row>
        <v-col xs="12" class="d-flex justify-center aligm-center pa-4">
            <img src="https://github.com/felipeazsantos.png" width="150" class="perfil-image" />
        </v-col>
    </v-row>
    <v-row>
      <v-col xs="12" class="d-flex align-center justify-center">
        <div class="mx-16 text-center">
          Profissional com 5 anos de experiência em desenvolvimento de software
          Atuei com tecnologias back-end e front-end.<br>
          Estou sempre em busca em me desenvolver como profissional, estudando e aplicando tudo que aprendo.
        </div>
      </v-col>
    </v-row>
    <v-row>
      <v-col xs="12">
        <Technologies />
      </v-col>
    </v-row>
     <v-row>
      <v-col>
        <h2 class="indigo--text text--darken-2 text-center">Onde trabalhei</h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <h2 class="indigo--text text--darken-2 text-center">Projetos</h2>
      </v-col>
    </v-row>
     <v-row>
      <v-col>
        <h2 class="indigo--text text--darken-2 text-center">Contato</h2>
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