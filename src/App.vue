<template>
  <v-app>
    <v-main>
      <cv/>
    </v-main>
  </v-app>
</template>

<script>
import cv from './components/cv.vue'

export default {
  name: 'App',

  components: {
    cv,
  },

  data: () => ({
    //
  }),
}
</script>
