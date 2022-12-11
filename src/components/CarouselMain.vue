<template>
  <div>
    <v-carousel v-model="model">
      <v-carousel-item
          v-for="(item,i) in items"
          :key="i"
          :src="item.src"
          cycle
      >
        <v-row
            class="fill-height text_color"
            align="center"
            justify="center"
        >
          <v-col
              class="text-center"
              cols="12"
          >
            <h1 class="text-h4 font-weight-thin mb-4">
              TRAVEL
            </h1>
            <h4 class="subheading">
              Discover Your Life, Travel Where You Want!
            </h4>

          </v-col>
        </v-row>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          src: 'https://media.istockphoto.com/id/1282610198/photo/airplane-flying-on-tropical-summer-vacation.jpg?b=1&s=170667a&w=0&k=20&c=6zA6DOTOhgszSdaI7OmEWAeYjHl7SSNi59Fh63jGBx4=',
        },
        {
          src: 'https://picture.triptrus.com/image/2017/05/dampak-positif-traveling.jpg',
        },
        {
          src: 'https://dynamic-media-cdn.tripadvisor.com/media/photo-o/15/33/f9/a5/villasimius.jpg?w=1600&h=900&s=1/',
        },
        {
          src: 'https://www.sardegna-villa.it/media/w1240x742/37216.jpg',
        },
      ],
    }
  },
}
</script>

<style scoped>
.text_color{
  color: white;
}
</style>