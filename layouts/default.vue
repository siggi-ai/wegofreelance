<template>
  <v-app dark>
    <v-app-bar app>new website</v-app-bar>
    <v-toolbar flat app>
<v-toolbar-side-icon></v-toolbar-side-icon>
</v-toolbar>
  <v-main>
    <v-container>
     
    </v-container>
  </v-main>
  <v-navigation-drawer>hello drawer</v-navigation-drawer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
