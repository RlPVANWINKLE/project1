<template>
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="blue darken-4 white--text text-center"
      width="100%"
    >
    <v-row >
        <v-col md="4">
            <v-card-text>
                <v-btn
                v-for="icon in icons"
                :key="icon"
                class="mx-4 white--text"
                icon
                >
                <v-icon size="24px">
                    {{ icon }}
                </v-icon>
                </v-btn>
            </v-card-text>
        </v-col>
        <v-col md="4">
            <v-card-text>
                <v-btn
                v-for="link in links"
                :key="link"
                class="mx-4 white--text"
                icon
                >               
                {{ link }}
                </v-btn>
            </v-card-text>      
        </v-col>  
        <v-col md="4">
            <v-card-text>
                <v-btn
                v-for="item in icon"
                :key="item"
                class="mx-4 white--text"
                icon
                >
                <v-icon size="24px">
                    {{ item }}
                </v-icon>
                </v-btn>
            </v-card-text>      
        </v-col>     
    </v-row> 
      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Ethan Strain</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>
<script>
  export default {
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
      links: [
          'Home',
          'Reviews',
          'FAQs',
      ],
      icon: [
          'mdi-phone',
          'mdi-email',
          'mdi-fax'
      ]
    }),
  }
</script>