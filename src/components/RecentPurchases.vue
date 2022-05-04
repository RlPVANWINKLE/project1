<template>
    <v-container fluid id="Recent Purchases">
        <h2 class="text-md-h3 text-sm-h4 text-h4 text-center mb-10">Recent Purchases</h2>
        <v-row justify="center" align="center">
            <v-col md="4" v-for="(car, index) in cars" :key="index" class="">
                <v-card  class="pt-10">
                    <v-img contain :src="car.img" height="30vh" class=""></v-img>
                    <v-card-title class="text-decoration-underline text-md-h5">{{car.Title}}</v-card-title>
                    <v-card-subtitle>Year: {{car.Year}}</v-card-subtitle>
                    <v-card-subtitle>Miles: {{car.Miles}}</v-card-subtitle>
                    <v-card-subtitle>Price: {{car.Price}}</v-card-subtitle>
                    <v-card-subtitle>Style: {{car.Style}}</v-card-subtitle>
                    <v-card-subtitle>Condition: {{car.Condition}}</v-card-subtitle>
                    <v-card-subtitle>Mpg: {{car.Mpg}}</v-card-subtitle>
                    <v-card-subtitle>Description: {{car.desc}}</v-card-subtitle>

                </v-card>
            </v-col>
        </v-row>

    </v-container>
</template>
<script>
export default {
    data(){
        return{
            cars:[
                {
                    Title: 'Toyota 4-Runner',
                    Year: '2001',
                    Miles: '179,000 miles',
                    Price: '$6,500',
                    Style: '4dr SR5 3.4L Auto',
                    Condition: '4 Stars',
                    Mpg: '17mpg city, 20mpg hw',
                    desc: 'I am the 2nd owner of this car just under 7 years ago. Original owner was a police officer who really maintained it well.  Reason for selling just upgraded to a 2017 4X4 for future endeavors.If youre looking for a work horse, this is it.',
                    img: require('../images/toyota_4runner.png')
                },
                {
                    Title: 'Ford Fusion',
                    Year: '2010',
                    Miles: '59,000 miles',
                    Price: '$8,919',
                    Style: '4dr Sedan SE FWD',
                    Condition: '5 stars',
                    Mpg: '22mpg city, 31mpg hw',
                    desc: 'Vehicle is low miles and in excellent shape…has only been driven locally in the past 2 years. I was a former Ford employee and the vehicle has been taken care of great. It has tinted windows, interior is spotless. Great first car!',
                    img: require('../images/ford_fusion.png')
                },
                {
                    Title: 'Honda Civic',
                    Year: '2013',
                    Miles: '131,092 miles',
                    Price: '$7,900',
                    Style: '4dr Sedan Auto LX FWD',
                    Condition: '3 stars',
                    Mpg: '28mpg city, 39mpg hw',
                    desc: 'Been my commuter since 2014, stereo replaced with a Boss unit with android auto and apple carplay along with speakers. Been very reliable but need larger vehicle for growing family.',
                    img: require('../images/honda_civic_sedan.png')
                }
            ]
        }
    }
}
</script>