<template>
  <v-row justify="center" align="center">
    <v-col
      v-for="social in socials"
      :key="social.title"
      :cols="12 / socials.length"
    >
    <v-row justify="center" align="center">

      <v-tooltip top color="info">
        <template v-slot:activator="{ on, attrs }">
          <v-btn icon v-bind="attrs" v-on="on" color="white" id="socialButton" :href="social.link" target="_blank">
            <v-avatar>
              <v-img :src="social.img"></v-img>
            </v-avatar>
          </v-btn>
        </template>
        <span
          ><strong>{{ social.title }}</strong></span
        >
      </v-tooltip>
    </v-row>

    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      socials: [
        {
          title: 'GitHub',
          img: '/githubLogo.png',
          link: 'https://github.com/Thaekeh'
        },
        {
          title: 'Stack Overflow',
          img: 'StackOverflow-logo.png',
          link: 'https://stackoverflow.com/users/14109713/thaeke-hekkenberg'
        },
        {
          title: 'LinkedIn',
          img: 'LinkedIn-logo.png',
          link: 'https://www.linkedin.com/in/thaeke-hekkenberg'
        },
      ],
    }
  },
}
</script>

<style lang="scss">
#itemContainer {
    margin-left: auto;
}

#socialButton {
    opacity: 0.8;
}

#socialButton:hover {
    opacity: 1;
    transform: scale(1.1);
}
</style>