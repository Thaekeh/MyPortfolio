<template>
  <v-container>
    <v-app-bar
      fixed
      app
      color="#FEFAF6"
      elevate-on-scroll
      id="navbar"
      v-anime="{
        opacity: 1,
        duration: 2000,
        delay: 1000,
        loop: false,
      }"
    >
      <v-toolbar-title id="toolbarTitle" @click="goTo('#top')"
        >Thaeke Hekkenberg</v-toolbar-title
      >
      <v-spacer></v-spacer>

      <span id="navbarIconContainer" class="hidden-sm-and-down">
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              class="navbarIcon"
              icon
              to="https://github.com/Thaekeh"
              v-bind="attrs"
              v-on="on"
            >
              <v-icon>mdi-github</v-icon>
            </v-btn>
          </template>
          <span>Github</span>
        </v-tooltip>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              class="navbarIcon"
              icon
              to="https://stackoverflow.com/users/14109713/thaeke-hekkenberg"
              v-bind="attrs"
              v-on="on"
            >
              <v-icon>mdi-stack-overflow</v-icon>
            </v-btn>
          </template>
          <span>Stack Overflow</span>
        </v-tooltip>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              class="navbarIcon"
              icon
              to="https://www.linkedin.com/in/thaeke-hekkenberg"
              v-bind="attrs"
              v-on="on"
            >
              <v-icon>mdi-linkedin</v-icon>
            </v-btn>
          </template>
          <span>LinkedIn</span>
        </v-tooltip>
      </span>

      <span class="hidden-sm-and-down">
        <v-btn text class="navbarLink" @click="goTo('#work')"> Work </v-btn>
        <v-btn text class="navbarLink" @click="goTo('#about')">
          About Me
        </v-btn>
        <v-btn text class="navbarLink" @click="goTo('#contact')">
          Contact
        </v-btn>
      </span>
      <v-app-bar-nav-icon
        @click="overlay = !overlay"
        class="hidden-md-and-up"
      ></v-app-bar-nav-icon>
    </v-app-bar>
    <v-overlay v-model="overlay" id="menuOverlay" opacity="0.8">
      <v-list id="list">
        <v-list-item class="menuListItem" @click="goTo('#top')">
          Home
        </v-list-item>
        <v-list-item class="menuListItem" @click="goTo('#work')">
          Work
        </v-list-item>
        <v-list-item class="menuListItem" @click="goTo('#about')">
          About
        </v-list-item>
        <v-list-item class="menuListItem" @click="goTo('#contact')">
          Contact
        </v-list-item>
        <v-list-item class="menuListItem"> </v-list-item>
        <v-list-item class="menuListItem">
          <v-btn icon @click="overlay = !overlay">
            <v-icon large> mdi-close </v-icon>
          </v-btn>
        </v-list-item>
      </v-list>
    </v-overlay>
  </v-container>
</template>

<script>
var VueScrollTo = require('vue-scrollto')

export default {
  data() {
    return {
      overlay: false,
    }
  },
  methods: {
    goTo(goal) {
      if (!this.$route.params.slug) {
        VueScrollTo.scrollTo(goal, 700)
      } else {
        this.$router.push({ path: `/` })
        setTimeout(() => {
          VueScrollTo.scrollTo(goal, 700)
        }, 1000)
      }
      this.drawer = false
    },
    scroll(goal) {
      VueScrollTo.scrollTo(goal, 700)
    },
  },
}
</script>

<style lang="scss" scoped>
#toolbarTitle {
  font-family: 'Montserrat', sans-serif;
  font-weight: 500;
  &:hover {
    cursor: pointer;
    text-decoration: underline;
  }
}

.navbarLink {
  font-family: 'Montserrat', sans-serif;
  font-weight: 500;
  &:hover {
    text-decoration: underline;
  }
}

#navbar {
  opacity: 0;
}

.menuListItem {
  background-color: rgba(0, 0, 0, 0);
  padding: 20px;
  font-size: 32px;
  font-weight: 500;
  justify-content: center;
  justify-items: center;
  text-align: center;
}
#list {
  background-color: rgba(0, 0, 0, 0);
}

.navbarIcon {
  opacity: 0.6;
  transition: all 0.1s ease-in-out;
  &:hover {
    opacity: 1;
    transition: all 0.1s ease-in-out;
  }
}

#navbarIconContainer {
  margin-right: 30px;
}
</style>