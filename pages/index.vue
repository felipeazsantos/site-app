<template>
  <v-container class="mt-16 px-16">
    <About class="mb-16" />
    <Technologies class="mb-16" />
    <WorketAt class="mb-16" />
    <Projects class="mb-16" />
    <Contact class="mb-16" />
  </v-container>
</template>

<script lang="ts">
import About from "@/components/home/About.vue";
import Technologies from "@/components/home/Technologies.vue";
import WorketAt from "@/components/home/WorketAt.vue";
import Projects from "@/components/home/Projects.vue";
import Contact from "@/components/home/Contact.vue";

export default {
  components: { About, Technologies, WorketAt, Projects, Contact },
  head() {
    return {
      title: "Felipe Azevedo dos Santos - Portfólio",
    };
  },
};
</script>

<style>
.perfil-image {
  border-radius: 10px 10px 40px 10px;
}
</style>