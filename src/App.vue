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
    </v-app>
</template>

<script>
export default {
  name: 'App',
  components: {

  }

}
</script>

<style>

</style>
