<template>
  <v-app>
    <v-navigation-drawer app permanent expand-on-hover mini-variant dark>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link :href="item.link">
          <v-list-item-icon>
            <v-icon size="30">{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>
              <span class="menu-item-title">{{ item.title }}</span>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    

    <v-main>
      <Nuxt />
    </v-main>

    <v-footer app>
      <Footer />
    </v-footer>

  </v-app>
</template>

<script lang="ts">
import Footer from '@/components/home/Footer.vue'

export default {
  name: "DefaultLayout",
  components: { Footer },
  data() {
    return {
      drawer: false,
      items: [
          { title: 'Sobre', icon: 'mdi-account-eye-outline', link: "#about" },
          { title: 'Tecnologias', icon: 'mdi-code-tags', link: "#technologies" },
          { title: 'Experiência', icon: 'mdi-badge-account-horizontal-outline', link: "#worketAt" },
          { title: 'Projetos', icon: 'mdi-widgets', link: "#projects" },
          { title: 'Contato', icon: 'mdi-email-outline', link: "#contact" },
        ],
      right: null,
    };
  },
};
</script>

<style>

 .menu-item-title {
    font-size: 16px;
 }
</style>