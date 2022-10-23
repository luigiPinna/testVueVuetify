<template>
  <v-app-bar app light flat class="px-8">
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