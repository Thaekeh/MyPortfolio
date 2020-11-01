<template>
    <v-app-bar fixed app color="#FEFAF6" flat>
      <v-toolbar-title id="toolbarTitle">Thaeke Hekkenberg</v-toolbar-title>
      <v-spacer></v-spacer>
      <span class="hidden-sm-and-down">
        <v-btn text class="navbarLink" href="#work"> Work </v-btn>
        <v-btn text class="navbarLink" href="#about"> About Me </v-btn>
        <v-btn text class="navbarLink" href="#contact"> Contact </v-btn>
      </span>
      <v-app-bar-nav-icon class="hidden-md-and-up"></v-app-bar-nav-icon>
    </v-app-bar>
</template>

<style lang="sass" scoped>
#toolbarTitle
  font-family: 'Montserrat', sans-serif
  font-weight: 500

.navbarLink
  font-family: 'Montserrat', sans-serif
  font-weight: 500  
</style>