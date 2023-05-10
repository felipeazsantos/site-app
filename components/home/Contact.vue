<template>
    <div>
      <SectionTitle title="Contato" id="contact" />

      <form @submit.prevent="submit" class="mt-16">
            <v-textarea
              autocomplete="email"
              label="Mensagem:"
              placeholder="Digite a sua mensagem, assim que receber respondo :D"
              v-model="message"
              height="60"
            ></v-textarea>

          <v-btn
            class="mr-4"
            type="submit"
          >
            Enviar
          </v-btn>
          <v-btn>
            Limpar dados
          </v-btn>
        </form>
    </div>
</template>

<script>
import SectionTitle from './SectionTitle.vue'

export default {
  components: {SectionTitle},
  data() {
    return {
      message: ''
    }
  }

}
</script>

<style>

</style>