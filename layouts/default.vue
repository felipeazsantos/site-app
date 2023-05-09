<template>
  <v-app>
    <v-navigation-drawer app permanent expand-on-hover mini-variant dark>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
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