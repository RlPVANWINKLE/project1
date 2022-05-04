<template>
  <v-container fluid>
      <h2 class=" text-md-h3 text-center white--text text-decoration-underline ">Testimonials</h2>
      <v-carousel class="mt-md-10" :continuous="true" hide-delimiters show-arrows-on-hover>
        <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            reverse-transition="fade-transition"
            transition="fade-transition"
        >
        <v-card width="25vw" height="50vh" class="mx-auto pt-md-10 rounded-xl">
            
            <v-img contain height="45%" class="" :src="item.src"></v-img>
            <v-card-title class="text-md-h4 mx-md-auto">{{item.name}}</v-card-title>
            <v-card-text class="">{{item.review}} </v-card-text>
            <v-row justify="center">
              <v-icon v-for="i in item.stars" :key="i" large color="amber" class="">mdi-star</v-icon>
            </v-row>
            
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
            src: require('../images/KYLE.jpg'),
            name: 'B. Drake, Billings MT ',
            review: 'Honest business. They gave clear explanation every step of their process, even allowing you to be there during inspection of your vehicle. Safest way to sell a car I have ever experienced. ',
            stars: 4
          },
          {
            src: require('../images/eric.jpg'),
            name: 'M. Hubbard, Phoenix AZ',
            review: 'My experience at Cardeal went very well. The manager was very professional, kind, and completely honest in making the offer for my vehicle. I would highly recommend Cardeal for anyone selling their vehicle. ',
            stars: 4
          },
          {
            src: require('../images/greage.jpg'),
            name: 'T. Hogan, Alexandria VA',
            review: 'WOW! Above and beyond service provided by Cardeal. They provided myself and my wife exceptional service and a reasonable price for my 2004 Jeep Cherokee. When we are ready to sell another car Cardeal will be our first option. Thank you Cardeal',
            stars: 5
          },
          {
            src: require('../images/kyle2.jpg'),
            name: 'H. Furlano, Atlanta GA',
            review: 'Very pleased. In all honesty I had my doubts it would be this easy to sell my car to anyone let alone Cardeal or any other online service. But they are on the up and up.  I would recommend this site to anyone who wishes to sell their car quickly. Thank you Cardeal!',
            stars: 5
          },
          {
            src: require('../images/kyler.jpg'),
            name: 'T. Moore, Denver CO',
            review: 'They were very prompt and when they gave me a quote they stood behind it. Communication throughout the whole process was awesome. They picked up my car at my home which was convenient for me since I have three young kids. My overall experience was great. '
            ,
            stars: 4
          }
        ],
        cycle: true,
      }
    },
  }
</script>