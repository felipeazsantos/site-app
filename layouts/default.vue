<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" app>
      <v-list-item>
        <v-list-item-content>
           <v-avatar class="pa-2" size="80">
             <img src="https://github.com/felipeazsantos.png"  />
          </v-avatar>
          <v-list-item-title class="text-h6 text-center"> Portfólio </v-list-item-title>
          <v-list-item-subtitle class="text-center"> Felipe Azevedo dos Santos </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon size="32">{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>
              <span class="menu-item-title">{{ item.title }}</span>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>

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
      drawer: null,
      items: [
          { title: 'Home', icon: 'mdi-home-circle-outline' },
          { title: 'Experiência', icon: 'mdi-book-account-outline' },
          { title: 'Projetos', icon: 'mdi-code-tags' },
          { title: 'Sobre', icon: 'mdi-help-box' },
          { title: 'Contato', icon: 'mdi-email-outline' },
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