<template>
  <div>
    <v-row>
      <v-col>
        <h2 class="grey--text text--darken-2 text-center pb-4 text-uppercase">
          Projetos
        </h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="d-flex justify-center align-center px-2 flex-wrap">
        <v-hover
          v-slot="{ hover }"
          v-for="project in projects"
          :key="project.name"
          class="my-2"
        >
          <v-card
            :elevation="hover ? 12 : 2"
            class="mx-auto"
            height="300"
            max-width="300"
            width="300"
          >
            <v-card-text class="my-4 text-center text-h6">
              {{ project.name }}
            </v-card-text>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: "Vue todo list",
          description: "",
          picture: "",
          technologies: [],
        },
        {
          name: "Vue todo list2",
          description: "",
          picture: "",
          technologies: [],
        },
        {
          name: "Vue todo list3",
          description: "",
          picture: "",
          technologies: [],
        },
        {
          name: "Vue todo list4",
          description: "",
          picture: "",
          technologies: [],
        },
        {
          name: "Vue todo list5",
          description: "",
          picture: "",
          technologies: [],
        },
        {
          name: "Vue todo list6",
          description: "",
          picture: "",
          technologies: [],
        },
        {
          name: "Vue todo list7",
          description: "",
          picture: "",
          technologies: [],
        },
        {
          name: "Vue todo list8",
          description: "",
          picture: "",
          technologies: [],
        },
        {
          name: "Vue todo list9",
          description: "",
          picture: "",
          technologies: [],
        },
      ],
    };
  },
};
</script>

<style>
</style>