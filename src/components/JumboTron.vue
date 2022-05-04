<template>
    <v-container fluid >
    <v-card  >
        <v-img src="../images/accident.jpg" max-height="90vh">        
      <!-- <v-img contain src="../images/Capture.jpg" max-width="25%" class="mx-auto"></v-img> -->
      
      <v-form v-model="valid">
          <v-card-title justify="center" class="justify-center text-md-h3 text-decoration-underline white--text mt-md-10">We Buy 'Any' Car</v-card-title>
            <v-container >
            <v-row justify="center" class="mt-md-10">
                <v-col cols="12" md="4" class="white rounded ma-2">
                <v-text-field
                    v-model="Vin"
                    :rules="VinRules"
                    :counter="17"
                    label="VIN"
                    required
                    
                ></v-text-field>
                </v-col>

                <v-col cols="12" md="4" class="white rounded ma-2">
                <v-select
                    v-model="select"
                    :items="make"
                    :rules="[v => !!v || 'Make is required']"
                    label="Make"
                    required
                ></v-select>
                </v-col>
                </v-row>
                <v-row justify="center" class="mt-md-10">
                <v-col cols="12" md="4" class="white rounded ma-2">
                <v-select
                    v-model="select"
                    :items="year"
                    :rules="[v => !!v || 'Model is required']"
                    label="Year"
                    required
                ></v-select>
                </v-col> 
                <v-col cols="12" md="4" class="white rounded ma-2">
                    <v-text-field
                    v-model="model"
                    label="Model"
                    required
                    ></v-text-field>
                </v-col>
                </v-row>
            </v-container>
            <div class="text-center mt-md-10">
                <v-btn rounded color="amber">Submit</v-btn>
            </div>
    </v-form>
  </v-img>
</v-card>

  </v-container>
</template>
<script>
import {make} from '../components/DataFile.js'
import {year} from '../components/DataFile.js'
  

  export default {
    data: () => ({
      valid: false,
      Vin: '',
      model: '',
      VinRules: [
        v => !!v || 'Vin is required',
        v => v.length == 17 || 'Vin Must be 17 digits',
      ],
      make,
      year,

    }),
  }
</script>