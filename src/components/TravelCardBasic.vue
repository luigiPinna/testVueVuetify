<template>
  <v-container fluid>
  <v-row :key="tours.length"
         :listData="tours"
         align="center" class="mx-0"
          >

    <v-col cols="12" sm="3" :index="i" :key="i" v-for="(tour, i) in this.tours">
      <v-hover
          v-slot="{hover}"
      >

      <v-card
          class="mx-auto"
          max-width="344"
          variant="tonal"
          :height="400"
          :elevation="hover ? 16:2" :class="{'on-hover' : hover}"

      >
        <figure>
          <v-img
              :src="'https://offtracktravel.ca/wp-content/uploads/2020/02/travel-call-to-action.jpg.webp'"
              height="200px"
          >
          </v-img>
        </figure>

        <v-card-title>
          {{ tour.email }}
        </v-card-title>

        <v-card-subtitle>
          {{ tour.first_name }}
        </v-card-subtitle>

        <v-card-actions>
          <v-btn
              color="orange lighten-2"
              text
          >
            <v-btn text color="orange"> EXPLORE </v-btn>
          </v-btn>

          <v-spacer></v-spacer>

          <v-btn
              icon
              @click="show = !show"
          >
            <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-expand-transition>
          <div v-show="show">
            <v-divider></v-divider>

            <v-card-text>
              tour.email
            </v-card-text>
          </div>
        </v-expand-transition>
      </v-card>
      </v-hover>

    </v-col>
  </v-row>
  </v-container>

</template>


<script>

export default {
  name: "TravelCardBasic",
  data() {
    return {
      tours: [],
      alignments: [
        'start',
        'center',
        'end',
      ],
      show: false,
    }
  },
  methods: {
    async fetchTravels() {
      // GET request using fetch with async/await
      const response = await fetch("https://reqres.in/api/users?");
      const data = await response.json();
      this.tours = data.data;
      console.log(this.tours)
    },
  },
  mounted() {
    this.fetchTravels()
  },
}
</script>

