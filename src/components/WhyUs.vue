<template>
    <v-container fluid class="mt-md-15" id="Why Us">
        <v-card class="">
            <v-card-title class=" justify-center text-md-h3 text-sm-h4 text-h4 text-decoration-underline">Why Choose Us?</v-card-title>
            <v-row justify="center" class="mt-md-10">
                <v-col v-for="(card, index) in cards" :key="index" md="3">
                    <v-card hover >
                        <v-card-title>{{card.title}}</v-card-title>
                        <v-img height="30vh" :src="card.img"></v-img>
                        <v-card-text>{{card.desc}}</v-card-text>
                    </v-card>
                </v-col>
            </v-row>
        </v-card>
    </v-container>
</template>

<script>
export default {
    data(){
        return{
            cards :[
                {
                    title:'Cash For Junk Cars & Trucks',
                    img: require('../images/car.jpg'),
                    desc:'We will offer the best cash price for your used or junk car… period. We buy all years, makes, models and in any condition! '
                },
                {
                    title:'We Pick Up Your Junker for Free',
                    img: require('../images/tow.jpg'),
                    desc:'Our junker removal specialists pickup your vehicle for free & will help you with all the documentation. '
                },
                {
                    title:'Fast On-the-Spot Cash for Cars',
                    img: require('../images/cash.jpg'),
                    desc:'Not only can you get paid in 48-72hrs, but also we guarantee the best price for your used car. Period. '
                }
            ]
        }
    }
}
</script>
