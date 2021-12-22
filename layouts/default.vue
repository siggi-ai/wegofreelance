<template>
  <v-app dark>

    <v-btn color="darkblue" dark @click.stop="drawer = !drawer">open/close drawer</v-btn>

  <v-navigation-drawer v-model="drawer" absolute temporary>
    <br>
    <br>
    <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;list</p>
  </v-navigation-drawer>

  <v-card class="input">
     <form>
      <label for="fname">First name:</label><br>
      <input type="text" id="fname" name="fname"><br>
      <label for="lname">Last name:</label><br>
      <input type="text" id="lname" name="lname">
    </form> 
  </v-card>

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

<style>
.input {
  margin: 0 auto;
  margin-top: 20px;
  width: 20%;
  padding: 20px;
}
</style>