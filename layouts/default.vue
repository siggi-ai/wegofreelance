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
        :rules="VornameRules"
        :counter="10"
        required
      ></v-text-field>
  
      <v-text-field
        v-model="Nachname"
        label="Nachname"
        :rules="NachnameRules"
        :counter="10"
        required
      ></v-text-field>

      <v-text-field
        v-model="Adresse"
        label="Adresse"
        :rules="AdresseRules"
        :counter="10"
        required
      ></v-text-field>

      <v-text-field
        v-model="Telefon"
        label="Telefon"
        :rules="TelefonRules"
        :counter="10"
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

      <v-btn
        color="warning"
        class="mr-4"
        @click="reset"
      >
        New User
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
      drawer: this.drawer,

      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',

      valid: true,
      Vorname: '',
      VornameRules: [
      v => !!v || 'Vorname is required',
      v => (v && v.length <= 10 && v.length > 2) || 'Vorname must be between 3 and 10 characters',
      ],
      Nachname: '',
      NachnameRules: [
      v => !!v || 'Nachname is required',
      v => (v && v.length <= 10 && v.length > 2) || 'Nachname must be between 3 and 10 characters',
      ],
      Adresse: '',
      AdresseRules: [
      v => !!v || 'Adresse is required',
      v => (v && v.length <= 20 && v.length > 2) || 'Adresse must be between 3 and 20 characters',
      ],
      Telefon: '',
      TelefonRules: [
      v => !!v || 'Telefon is required',
      ],
    }
  },
  methods: {
    submit () {
      let user = [this.Vorname, this.Nachname, this.Adresse, this.Telefon];
      console.log(user);
    },
    reset () {
      this.$refs.form.reset()
    },
  },
/*   computed: {
    drawer () {
      return this.$store.state.drawer;
    }
  } */
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