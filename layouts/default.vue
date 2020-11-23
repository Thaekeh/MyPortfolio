<template>
  <v-app id="top">
    <navbar></navbar>
    <v-main class="primary">
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar'

export default {
}
</script>

<style lang="sass" scoped>
html
  scroll-behavior: smooth
  background-color: #FEFAF6

body
  background-color: #FEFAF6
</style>
