<template>
  <v-container>
    <v-app-bar fixed app color="#FEFAF6" elevate-on-scroll id="navbar" v-anime="{
          opacity: 1,
          duration: 2000,
          delay: 1000,
          loop: false,
        }">
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
    <v-overlay v-model="drawer" id="menuOverlay" opacity="0.8">
      <v-list id="list">
        <v-list-item class="menuListItem" @click="goTo('home')">
          Home
        </v-list-item>
        <v-list-item class="menuListItem" @click="goTo('work')">
          Work
        </v-list-item>
        <v-list-item class="menuListItem" @click="goTo('contact')">
          Contact
        </v-list-item>
        <v-list-item class="menuListItem">
        </v-list-item>
        <v-list-item class="menuListItem">
          <v-btn icon @click="drawer = !drawer">
            <v-icon>
              mdi-close
            </v-icon>
          </v-btn>
        </v-list-item>
      </v-list>
    </v-overlay>
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
    </v-navigation-drawer> -->
  </v-container>
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
      this.drawer = false
    }
  }
}
</script>

<style lang="sass" scoped>
#toolbarTitle
  font-family: 'Montserrat', sans-serif
  font-weight: 500
  cursor: pointer
  &:hover
    text-decoration: underline

.navbarLink
  font-family: 'Montserrat', sans-serif
  font-weight: 500
  &:hover
    text-decoration: underline

#navbar
  opacity: 0

.menuListItem
  background-color: rgba(0, 0, 0, 0)
  padding: 20px
  font-size: 32px
  font-weight: 500
  justify-content: center
  justify-items: center
  text-align: center

#list
  background-color: rgba(0, 0, 0, 0)
</style>