<template>
    <v-container class="mt-md-10 mt-sm-5" id="How It Works">
        <h2 class=" text-md-h3 text-sm-h4 text-center white--text text-decoration-underline ">How It Works</h2>
        <v-col>
            <v-card v-for="(card, index) in cards" :key="index" width=auto class="mx-auto my-md-2 my-sm-2 my-2">
                <v-card-title>{{card.num}} - {{card.title}}</v-card-title>
                <v-card-text>{{card.description}}</v-card-text>
                
            </v-card>
        </v-col>
    </v-container>
</template>
<script>
export default {
    data(){
        return{
            cards:[
                {
                    num: '#1',
                    title: 'Fill out a form that provides accurate information about your car (i.e., VIN, year, make, model, mileage, condition of car, accidents',
                    
                },
                {
                    num: '#2',
                    title: 'Get an instant offer on your car that is good for 7 days.',
                },
                {
                    num: '#3',
                    title: 'Provide access to car.  Deliver car to closest cardeal location or have us come get it.',
                },
                {
                    num: '#4',
                    title: 'Provide title proving your ownership of the vehicle.',
                },
                {
                    num: '#5',
                    title: 'Cardeal will inspect your car to verify its condition.',
                },
                {
                    num: '#6',
                    title: 'If everything checks out, you can decide if you want to accept the offer.  You can go with cash or apply the money to a trade in.',
                }
            ]
        }
    }
}
</script>