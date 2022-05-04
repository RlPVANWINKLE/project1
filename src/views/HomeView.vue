<template>
  <div class="grey" id="Home">
    <jumbo/>
    <how/>
    <why/>
    <test/>
    <Faq/>
    <recent/>
  </div>
</template>

<script>
import Jumbo from '../components/JumboTron.vue'
import How from '../components/HowItWorks.vue'
import Why from '../components/WhyUs.vue'
import Test from '../components/TestimonialsView.vue'
import Faq from '../components/FaQ.vue'
import Recent from '../components/RecentPurchases.vue'
  

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
      Faq,
      Recent,
    }
  }
</script>
