<template>
    <div>
        <ul class="technologies-list">
            <li class="technologies-items" v-for="technologie in technologies" :key="technologie">
                <v-sheet outlined class="d-flex flex-column justify-center align-center pa-10" :style="'border-bottom: 4px solid ' + technologie.color">
                    <img :src="technologie.picture" width="80" :alt="technologie.name" />
                    <span class="font-weight-bold">{{ technologie.name }}</span>
                </v-sheet>
            </li>
        </ul>
    </div>
</template>

<script lang="ts">
export default {
    data() {
        return {
        technologies: [
                {name: 'Vue.js', color: "#54AE54", picture: require('@/assets/vuejs.png') },
                {name: 'React.js', color: "#AB2353", picture: require('@/assets/reactjs.png') },
                {name: 'Node.js', color: "#22DDFF", picture: require('@/assets/nodejs.png') },
            ]
        }
  }
}
</script>

<style>
    .technologies-list {
        list-style-type: none;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .technologies-items {
        padding: 12px 12px;
    }
</style>