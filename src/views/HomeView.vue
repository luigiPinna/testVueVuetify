<template>
  <v-app :style="{ background: $vuetify.theme.themes.light.background}">
    <navbar/>
  </v-app>

</template>

<script>
  import Navbar from "@/components/Navbar";

  export default {
    name: 'Home',

    components: {
      Navbar,
    },
  }
</script>
