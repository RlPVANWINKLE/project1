<template>
    <v-card width="98vw" class="mx-auto mb-10 mt-md-15" id="FAQs" >
        <h2 class="text-md-h3 text-sm-h4 text-h4 text-center text-decoration-underline pa-md-10 pa-sm-5 pa-2">FAQ's</h2>
        <v-list>
            <v-list-group ripple="true"
                v-for="(item,index) in questions"
                :key="index"
                v-model="item.active"
                no-action
            >
                <template v-slot:activator>
                <v-list-item-content >
                    <v-list-item-title v-text="item.Question" class="text-md-h5 border pt-md-7 pt-sm-7 pt-7"></v-list-item-title>
                </v-list-item-content>
                </template>

                <v-list-item style="width: 90%">
                <v-list-item-content v-text="item.Answer" class="text-md-h5">
                </v-list-item-content>
                </v-list-item>
            </v-list-group>
        </v-list>
    </v-card>
</template>
<script>
export default {
    data(){
        return{
            questions:[
                {
                    Question: 'How is Cardeal different from other online car buyers?',
                    Answer: 'Cardeal will buy "any" car even if it has a blown engine.  At Cardeal we want to offer the highest value, quick payment for cars, convenience, and a secure transaction. If you sell us your car, you are not obligated to buy your next car from us although we promise that if you do you will get a great deal.'
                },
                {
                    Question: 'How is the price of my car calculated?',
                    Answer: 'Prices are calculated based on the current market value of your car and its condition.'
                },
                {
                    Question: 'What costs will I be responsible for?',
                    Answer: 'Cardeal is a free service. There are no charges for evaluations and offers. If you sell a car with Cardeal, we pay for pick up and towing. We have no hidden costs.'
                },
                {
                    Question: 'How quickly can you have my vehicle picked up?',
                    Answer: 'Cardeal has a branch in every state. Therefore, we can usually pick up your vehicle within 24 to 48 hours after you accept our offer.'
                },
                {
                    Question: 'What type of documentation will I need to provide?',
                    Answer: 'When filling out the online form, you will be asked to enter your Vehicle Identification Number (VIN).  A vehicle’s VIN contains its year, make, model, trim information and other auto options and details. Cardeal also requires a title in the seller’s name. We cannot buy your vehicle without a valid, signed title from the registered vehicle owner'
                },
                {
                    Question: 'Will you buy my car if I cant get it started?',
                    Answer: 'If you have a damaged, wrecked or non-running car on your hands, Cardeal can help you get rid of it. We’ll give you a fair market offer for your car that’s tailored to your vehicle’s conditions and local market demands.'
                },
            ]
        }
    }
}
</script>
<style scoped>
.border{
    border-top: 1px solid gray;
}
</style>