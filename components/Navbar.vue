<template>
  <!-- <v-container> -->
    <v-app-bar fixed app color="#FEFAF6" flat>
      <v-toolbar-title id="toolbarTitle" @click="goTo('home')">Thaeke Hekkenberg</v-toolbar-title>
      <v-spacer></v-spacer>
      <span class="hidden-sm-and-down">
        <v-btn text class="navbarLink"  @click="goTo('work')"> Work </v-btn>
        <v-btn text class="navbarLink"  @click="goTo('about')"> About Me </v-btn>
        <v-btn text class="navbarLink" @click="goTo('contact')"> Contact </v-btn>
      </span>
      <v-app-bar-nav-icon
        @click="drawer = !drawer"
        class="hidden-md-and-up"
      ></v-app-bar-nav-icon>
    </v-app-bar>
    <!-- <v-navigation-drawer v-model="drawer" absolute temporary color="primary">
      <v-list nav dense>
        <v-list-item-group
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item class="text-center">
            <v-list-item-title>Foo</v-list-item-title>
          </v-list-item>

          <v-list-item class="text-center">
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>

          <v-list-item class="text-center">
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </v-container> -->
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
    }
  },
  methods: {
    goTo(goal) {
      if (!this.$route.params.slug) {
        this.$router.push('#' + goal)
      } else {
        this.$router.push({path: `/#${goal}`})
      }
    }
  }
}
</script>

<style lang="sass" scoped>
#toolbarTitle
  font-family: 'Montserrat', sans-serif
  font-weight: 500
  cursor: pointer

.navbarLink
  font-family: 'Montserrat', sans-serif
  font-weight: 500
</style>