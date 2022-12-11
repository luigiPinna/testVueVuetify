<template>
  <div>
      <v-app-bar light>
        <v-app-bar-nav-icon @click="drawer = true"
                            class="d-flex d-sm-none"
        ></v-app-bar-nav-icon>
        <v-toolbar-title>Travel App</v-toolbar-title>
        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>

        <template v-slot:extension>
          <v-tabs
              v-model="tab"
              align-with-title
              class="d-none d-sm-flex"
          >
          <v-tabs-slider color="grey"></v-tabs-slider>

          <v-tab
              v-for="item in items"
              :key="item"
          >
            {{ item }}
          </v-tab>
          </v-tabs>
        </template>
      </v-app-bar>
      <!-- Add a navigation bar -->
      <v-navigation-drawer
          v-model="drawer"
          absolute
          temporary
      >
        <v-list
            nav
            dense
        >
          <v-list-item-group
          >
            <v-list-item v-for="(item, index) in items">
              <v-list-item-title @click="tab = index">{{ item }}</v-list-item-title>
            </v-list-item>

          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>

  </div>
</template>


<script>
export default {
  data: () => ({
    drawer: false,
    tab: null,
    items: [
      'home', 'offers', 'destinations', 'about', 'news',
    ],
})
}
</script>

<style scoped>
.light{
  background: None;
}
</style>