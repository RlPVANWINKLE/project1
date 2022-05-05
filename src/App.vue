<template>
  <v-app >
    <nav-bar></nav-bar>
    <v-main class="text">
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import NavBar from './components/NavBar.vue'
export default {
  name: 'App',

  data: () => ({
    //
  }),
  components:{
    NavBar,
  }
};
</script>
<style scoped>
.text{
  word-break: normal;
}

</style>
