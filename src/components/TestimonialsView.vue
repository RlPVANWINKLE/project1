<template>
  <v-container fluid>
      <h2 class=" text-md-h3 text-center white--text text-decoration-underline ">Testimonials</h2>
      <v-carousel class="mt-md-10" :cycle="cycle" :continuous="false" hide-delimiters show-arrows-on-hover>
        <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            reverse-transition="fade-transition"
            transition="fade-transition"
        >
        <v-card width="25vw" height="75vh" class="mx-auto">
            
            <v-img contain height="45%" :src="item.src"></v-img>
            <v-card-title class="white">{{item.name}}</v-card-title>
            <v-card-text>{{item.review}} </v-card-text>
            
        </v-card>
        </v-carousel-item>
        </v-carousel>
  </v-container>
</template>
<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
            name: 'Jake',
            review: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim assumenda amet expedita exercitationem facere quis fuga perferendis alias neque! Excepturi doloremque impedit asperiores id sunt autem dolor ea quos rem.'
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
            name: 'Jake',
            review: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim assumenda amet expedita exercitationem facere quis fuga perferendis alias neque! Excepturi doloremque impedit asperiores id sunt autem dolor ea quos rem.'
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
            name: 'Jake',
            review: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim assumenda amet expedita exercitationem facere quis fuga perferendis alias neque! Excepturi doloremque impedit asperiores id sunt autem dolor ea quos rem.'
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
            name: 'Jake',
            review: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim assumenda amet expedita exercitationem facere quis fuga perferendis alias neque! Excepturi doloremque impedit asperiores id sunt autem dolor ea quos rem.'
          },
        ],
        cycle: true,
      }
    },
  }
</script>