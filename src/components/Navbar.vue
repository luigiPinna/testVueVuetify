<template>
  <v-app-bar flat class="px-8"
             color="white"
             elevate-on-scroll
             scroll-target="#scrolling-techniques-7">
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
    <v-btn icon>
      <v-icon color="#54aedb">fa-thin fa-sailboat</v-icon>
    </v-btn>

    <v-spacer></v-spacer>
    <v-btn text @click="scroll('about')">Home</v-btn>
    <v-btn text @click="scroll('project')">Services</v-btn>
    <v-btn text @click="scroll('about')">about</v-btn>
    <v-btn text @click="scroll('contact')"> contact</v-btn>
  </v-app-bar>
</template>


<script>
export default {

}
</script>

<style scoped>
.light{
  background: None;
}
</style>