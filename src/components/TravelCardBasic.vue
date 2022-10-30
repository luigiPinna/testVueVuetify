<template>

  <div>
      <v-container
          v-for="align in alignments"
          :key="align"
          class="grey lighten-5 mb-6"
      >
        <v-row
            :align="align"
            no-gutters
            style="height: 150px;"
        >
          <v-col

          >
            <v-card
                class="pa-2"
                outlined
                tile
            >
              <v-list dense>
                <v-list-item-group v-model="tours">
                  <v-list-item-group v-for="(tour, i) in tours" :key="i" >
                    <v-list-item-content>
                      <v-list-item-title>

                      </v-list-item-title>
                      <v-list-item-subtitle>

                      </v-list-item-subtitle>
                    </v-list-item-content>


                  </v-list-item-group>

                </v-list-item-group>


              </v-list>
                  <v-card-title> {{tour.data[i].email}}</v-card-title>

            </v-card>
          </v-col
             >
        </v-row>
      </v-container>
  </div>

</template>

<script>


export default {
  name: "TravelCardBasic",
  data: () => ({
    alignments: [
      'start',
      'center',
      'end',
    ],
    tours: [],
  }),
  mounted:
    async function (){
      const response = await fetch('https://reqres.in/api/users?page=2');
      this.tours = await response.json();
      console.log(this.tours.data[0].email)
      console.log("data: ", this.tours)
    }

}
</script>

