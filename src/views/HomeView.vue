<template>
  <v-app :style="{ background: $vuetify.theme.themes.light.background}">
    <navbar/>
    <v-container fluid>

      <mid-carousel/>

      <carousel-main/>

      <travel-card-basic/>

    </v-container>
  </v-app>

</template>

<script>
  import Navbar from "@/components/Navbar";
  import CarouselMain from "@/components/CarouselMain";
  import MidCarousel from "@/components/MidCarousel";
  import TravelCardBasic from "@/components/TravelCardBasic";

  export default {
    name: 'Home',

    components: {
      TravelCardBasic,
      MidCarousel,
      CarouselMain,
      Navbar,
    },
  }
</script>
