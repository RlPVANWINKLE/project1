<template>
  <v-app>
    <nav-bar></nav-bar>
    <v-main>
      <router-view/>
    </v-main>
    <Footer/>
  </v-app>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Footer from './components/FooterView.vue'
export default {
  name: 'App',

  data: () => ({
    //
  }),
  components:{
    NavBar,
    Footer,
  }
};
</script>
<style scoped>
body{
  background-color: gray;
}
</style>
