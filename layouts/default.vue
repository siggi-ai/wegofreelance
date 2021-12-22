<template>
  <v-app dark>

    <v-btn color="darkblue" dark @click.stop="drawer = !drawer">open/close drawer</v-btn>

  <v-navigation-drawer v-model="drawer" absolute temporary>
    <br>
    <br>
    <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;list</p>
  </v-navigation-drawer>

  <v-card class="input" color="blue">
     <v-form
      ref="form"
      v-model="valid"
      lazy-validation
    >
      <v-text-field
        v-model="Vorname"
        label="Vorname"
        required
      ></v-text-field>
  
      <v-text-field
        v-model="Nachname"
        label="Nachname"
        required
      ></v-text-field>

      <v-text-field
        v-model="Adresse"
        label="Adresse"
        required
      ></v-text-field>

      <v-text-field
        v-model="Telefon"
        label="Telefon"
        required
      ></v-text-field>
  
  
      <v-btn
        :disabled="!valid"
        color="success"
        class="mr-4"
        @click="submit"
      >
        Submit
      </v-btn>
  
    </v-form>
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
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',

      valid: true,
      Vorname: '',
      Nachname: '',
      Adresse: '',
      Telefon: '',
    }
  },
  methods: {
    submit () {
      let user = [this.Vorname, this.Nachname, this.Adresse, this.Telefon];
      console.log(user);
    },
  },
};
</script>

<style>
.input {
  margin: 0 auto;
  margin-top: 20px;
  width: 50%;
  padding: 20px;
  color: blue;
}
</style>