<template>
    <v-container class="mt-md-10">
        <h2 class=" text-md-h3 text-center white--text text-decoration-underline ">How It Works</h2>
        <v-col>
            <v-card v-for="(card, index) in cards" :key="index" width="50%" class="mx-auto my-md-2">
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
                    title: 'Vehicle Information',
                    description: 'Get started by pulling together your vehicle information and call or complete the anonymous form to get your top cash offer.'
                },
                {
                    num: '#2',
                    title: 'Set A Date',
                    description: 'Once we have an agreement on a fair, upfront cash offer, we arrange everything! A tow truck will be sent to your location and pays you on the spot.'
                },
                {
                    num: '#3',
                    title: 'Get Paid',
                    description: 'Once you are paid and the paperwork is completed, we tow the vehicle away and you’ll never have to deal with it again!'
                }
            ]
        }
    }
}
</script>