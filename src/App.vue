<template>
  <v-app :dark="darkTheme">
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Everyday Savant</span>
        <span class="font-weight-light">Labs</span>
        <!-- Try to move this around -->
        <v-switch v-model="darkTheme" label="Night mode"></v-switch>
      </v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <v-content>
      <HomePage/>
    </v-content>
  </v-app>
</template>

<script>
import HomePage from './components/HomePage'

export default {
  name: 'App',
  components: {
    HomePage
  },
  data () {
    return {
      darkTheme: true
    }
  }
}
</script>
