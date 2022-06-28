<template>
  <v-navigation-drawer
      v-model="drawer"
      app
    >
    <v-img 
      src="https://cdn.pixabay.com/photo/2022/06/03/03/50/beach-7239311_960_720.jpg"
      height="140"
      class="pa-4"
      >
      <div class="text-center">
          <v-avatar
            class="mb-4"
            color="grey darken-1"
            size="80"
          >
          <v-img src="https://cdn.pixabay.com/photo/2016/08/20/05/38/avatar-1606916_960_720.png"></v-img>
          </v-avatar>

          <div class="white--text">john@vuetifyjs.com</div>
       
      </div>
    </v-img>

      <v-divider></v-divider>

      <v-list>
        <v-list-item
          v-for="[icon, text] in links"
          :key="icon"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <!--  -->
    </v-navigation-drawer>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return {
        links: [
          ['mdi-inbox-arrow-down', 'Dashboard'],
          ['mdi-send', 'Profile'],
          ['mdi-delete', 'Product'],
          ['mdi-alert-octagon', 'Orders'],
        ],
    }
  },
  props: ["drawer"],
}
</script>

<style>

</style>