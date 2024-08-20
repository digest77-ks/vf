<template>
  <v-footer
    class="bg-indigo-lighten-1 text-center d-flex flex-column"
    :footer='footer'
    >
    <v-row justify="center" no-gutters>
      <v-col class="text-center mt-4" cols="12">
        {{ new Date().getFullYear() + ' ' + footer }} — <strong>Vuetify</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
  props: ['footer']
}
</script>
