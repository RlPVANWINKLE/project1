<template>
    <nav>
        <v-toolbar>
            <v-app-bar-nav-icon @click="side = !side"></v-app-bar-nav-icon>
            <span class="blue--text text--darken-4 text-md-h2 font-weight-black">Car</span>
            <span class="grey--text text-md-h2 font-weight-bold">Deal</span>
        </v-toolbar>
        <v-navigation-drawer app v-model="side" class="light-blue darken-4" >
            <v-img src="../images/Capture.jpg" max-width="75%" class="mx-auto mt-10 rounded-circle link" @click="side = !side"></v-img>
            <v-container  class="mt-5">
                <v-row v-for="(i, index) in list" :key="index" justify="center" class="mt-sm-10 py-2 mx-md-10 rounded-pill link" @click="side = !side">{{list[index]}}</v-row>
            </v-container>            
        </v-navigation-drawer>
    </nav>
</template>

<script>

export default {
    components: { 

     },
     data(){
         return{
             side: false,
             list: ['Home','How It Works','Why Us','Testimonials','FAQs', 'Recent Purchases']
         }
     }
}
</script>
<style scoped>
.link{
    color: white;
    background-color: rgb(180, 180, 180);
}
.link:hover{
    color: black;
    background-color: white;
    cursor: pointer;
}
</style>