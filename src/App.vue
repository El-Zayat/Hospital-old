<template>
  <v-app>
    <Navbar />
    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
import $ from 'jquery'
import niceScroll from 'jquery.nicescroll'
import Navbar from '@/components/Navbar'

export default {
  name: 'App',

  components: {
    Navbar
  },

  mounted() {
    $('html').niceScroll({
      cursorcolor: 'rgba(34, 34, 34, 0.85)',
      cursorborder: 'none'
    })
  },
};
</script>

<style lang="scss">
@import './assets/style/config';
</style>
