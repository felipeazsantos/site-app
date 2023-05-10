<template>
    <v-row>
        <v-col>
        <h2 class="blue--text text--darken-3 text-center pb-4">
            {{ title }}
        </h2>
        </v-col>
    </v-row>
</template>

<script>
export default {
    props: {
        title: String
    }
}
</script>

<style>

</style>