<template>
  <v-app id="inspire">
    
    <Sidebar :drawer="drawer"></Sidebar>
    <Header @toggleDrawer="drawer = !drawer"></Header>

    <v-main>
      <!--  -->
    </v-main>
  </v-app>
</template>

<script>
import Sidebar from './components/inc/Sidebar.vue';
import Header from './components/inc/Header.vue';
  export default {
    name: 'App',
    data(){
      return {
        drawer: true,
      }
    },
    components: {
      Sidebar,
      Header
    }
  }
</script>
<style>

</style>
