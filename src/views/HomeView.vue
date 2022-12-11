<template>
  <v-app :style="{ background: $vuetify.theme.themes.light.background}">
    <navbar/>
    <v-container fluid>

      <carousel-main/>
      <travel-card-basic/>

      <MainFooter/>

    </v-container>
  </v-app>

</template>

<script>
  import Navbar from "@/components/Navbar";
  import CarouselMain from "@/components/CarouselMain";
  import MidCarousel from "@/components/MidCarousel";
  import TravelCardBasic from "@/components/TravelCardBasic";
  import MainFooter from "@/components/MainFooter";

  export default {
    name: 'Home',

    components: {
      MainFooter,
      TravelCardBasic,
      MidCarousel,
      CarouselMain,
      Navbar,
    },
  }
</script>
