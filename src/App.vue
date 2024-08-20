<template>
  <v-card>
    <v-layout>
      <v-app-bar
          color="primary"
          prominent
        >
        <v-app-bar-nav-icon @click="drawer = !drawer" />
        <site-title :title='title'></site-title>
        <v-spacer></v-spacer>

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
        <site-menu></site-menu>
      </v-navigation-drawer>
      <router-view/>
    </v-layout>
    <site-footer :footer='footer'></site-footer>
  </v-card>
</template>

<script>
import SiteTitle from '@/views/site/TitleChange'
import SiteFooter from '@/views/site/FooterChange'
import SiteMenu from '@/views/site/MenuChange'

export default {
  name: 'App',
  components: {
    SiteTitle,
    SiteFooter,
    SiteMenu
  },
  data () {
    return {
      drawer: false,
      title: 'This is title',
      footer: 'Footer'
    }
  }

}
</script>

<style>

</style>
