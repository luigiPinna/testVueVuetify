<template>
  <v-app id="inspire">
    <v-navigation-drawer
        v-model="drawer"
        app
    >
      <!--  -->
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <v-carousel></v-carousel>
    </v-main>
  </v-app>
</template>

<script>
import Carousel from "@/components/carousel";
export default {
  components: {Carousel},
  data: () => ({ drawer: null }),
}
</script>