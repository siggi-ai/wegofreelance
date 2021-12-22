<template>
<div>
    <v-toolbar-side-icon></v-toolbar-side-icon>
    <v-navigation app v-model="drawer">
        <p>test</p>
    </v-navigation>
</div>
</template>

<script>
export default {
  data() {
      return {
          drawer: true
      }
  }
}
</script>