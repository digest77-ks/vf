<template>
  <v-card>
    <v-layout>
      <v-app-bar
          color="primary"
          prominent
        >
        <v-app-bar-nav-icon @click="drawer = !drawer" />
        <v-toolbar-title>My Pages</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon to='/about'>
          <v-icon>mdi-magnify</v-icon>
         </v-btn>
        <v-btn icon to='/'>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>
      </v-app-bar>
      <v-navigation-drawer v-model = "drawer">
         <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="title">
              Application
            </v-list-item-title>
            <v-list-item-subtitle>
              subtext
            </v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>
      </v-navigation-drawer>
      <router-view/>
    </v-layout>
        <v-footer
        class="bg-indigo-lighten-1 text-center d-flex flex-column"

      >
        <v-row justify="center" no-gutters>
          <v-col class="text-center mt-4" cols="12">
            {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
          </v-col>
        </v-row>
      </v-footer>
  </v-card>
</template>

<script>
export default {
  name: 'App',
  components: {

  },
  data () {
    return {
      drawer: false
    }
  }

}
</script>

<style>

</style>
