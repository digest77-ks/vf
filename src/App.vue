<template>
    <v-app>
      <v-container>
        <v-app-bar color='primary' dark >
          <v-app-bar-nav-icon/>
          <v-app-bar-title>Page Bar</v-app-bar-title>
          <v-spacer/>
          <v-btn icon to='/about'>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>
          <v-btn icon to='/'>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>
      </v-app-bar>
      </v-container>
      <v-main>
        <router-view/>
      </v-main>
      <v-footer
      class="bg-indigo-lighten-1 text-center d-flex flex-column"

    >
      <v-row justify="center" no-gutters>
        <v-btn
          v-for="link in links"
          :key="link"
          class="mx-2"
          color="white"
          rounded="xl"
          variant="text"
        >
          {{ link }}
        </v-btn>
        <v-col class="text-center mt-4" cols="12">
          {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
        </v-col>
      </v-row>
    </v-footer>
    </v-app>
</template>

<script>
export default {
  name: 'App',
  components: {

  },
  data: () => ({
    links: [
      'Home',
      'About Us',
      'Team',
      'Services',
      'Blog',
      'Contact Us'
    ]
  })

}
</script>

<style>

</style>
