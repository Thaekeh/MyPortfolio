<template>
  <v-app>
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
  data() {
    return {
    }
  },
}
</script>
