<template>
  <v-app>
    <!-- <v-navigation-drawer app> -->
      <!-- Sidebar navigation -->
    <!-- </v-navigation-drawer> -->

    <v-app-bar app>
      <!-- Top Navigation -->
      
      <!-- <v-spacer></v-spacer> -->

      <v-app-bar-title>Chuck Norris Questionnaire</v-app-bar-title>
      
      <v-spacer></v-spacer>

      <v-btn color="primary" to="/">Home</v-btn>
      <v-btn color="red" to="/about">About</v-btn>

      <v-spacer></v-spacer>

    </v-app-bar>

    <!-- Sizes your content based upon application components -->
    <v-main>

      <!-- Provides the application the proper gutter -->
      <v-container fluid>

        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App',

  data () {
    return {
      //
    }
  },
})
</script>
