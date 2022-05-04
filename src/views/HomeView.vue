<template>
  <div class="grey">
    <jumbo/>
    <how/>
    <why/>
    <test/>
  </div>
</template>

<script>
import Jumbo from '../components/JumboTron.vue'
import How from '../components/HowItWorks.vue'
import Why from '../components/WhyUs.vue'
import Test from '../components/TestimonialsView.vue'
  

  export default {
    data(){
      return{

      }
    },
    components:{
      Jumbo,
      How,
      Why,
      Test,
    }
  }
</script>
