<template>
  <div>
    <SectionTitle title="Projetos" />
    <v-row>
      <v-col class="d-flex justify-center align-center px-2 flex-wrap">
        <div v-for="project in projects" :key="project.name">
          <h3 class="blue--text text--accent-2 text-center mt-4">{{ project.name }}</h3>
          <v-hover v-slot="{ hover }" class="mt-4">
            <v-card
              :elevation="hover ? 12 : 2"
              class="mx-auto"
              height="300"
              max-width="300"
              width="300"
              :img="project.picture"
            >
            </v-card>
          </v-hover>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import SectionTitle from './SectionTitle.vue'

export default {
  components: {SectionTitle},
  data() {
    return {
      projects: [
        {
          name: "Vue todo list",
          description: "",
          picture: require("@/assets/vue-todo-list.jpg"),
          technologies: [],
        },
        {
          name: "Base de conhecimento",
          description: "",
          picture: "",
          technologies: ["Vue.js", "Node.js", "Express", "Consign", "Knex"],
        },
        {
          name: "Treinatweet",
          description: "",
          picture: "",
          technologies: ["React"],
        },
        {
          name: "Stock trader",
          description: "",
          picture: "",
          technologies: ["Vue.js", "Vuex", "Firebase", "Vuetify"],
        },
        {
          name: "Matador de Monstro",
          description: "",
          picture: "",
          technologies: ["Vue.js"],
        },
      ],
    };
  },
};
</script>

<style>
</style>