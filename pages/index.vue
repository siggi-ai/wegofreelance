<template>
<div>

  <v-app dark>
    <v-btn color="darkblue" dark @click.stop="drawer = !drawer">open/close drawer</v-btn>
  <v-navigation-drawer v-model="drawer" absolute temporary>
    <br>
    <br>
    <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;list</p>
  </v-navigation-drawer>
  </v-app>
  <v-card class="logo py-4 d-flex justify-center">
        <NavDrawer />
      </v-card>
  <p>hello world</p>
  
  
</div>
</template>

<script>
import NavDrawer from "@/components/NavDrawer.vue";

export default {
  name: 'IndexPage',
  components: { NavDrawer },
}
</script>
