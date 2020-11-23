<template>
  <v-container>
    <v-card
      id="greatCard"
      class="d-flex flex-column"
      hover
      v-for="(project, index) in projects"
      :key="project.title"
    >
      <v-row>
        <v-col xs="12" sm="6" md="6" id="inlayColumn" v-if="showLeft(index)">
          <v-card :color="project.color" id="inlayCard" height="100%">
            <v-container fluid fill-height>
              <v-col cols="12">
                <v-img :src="project.image" id="inlayImage"></v-img>
              </v-col>
            </v-container>
          </v-card>
        </v-col>

        <v-col xs="6" sm="6" md="6">
          <v-card-title
            class="justify-center projectCardTitle"
            :style="{ fontSize: fontSize + 'px' }"
            >{{ project.title }}</v-card-title
          >
          <v-card-text class="text-center">
            <v-row>
              <v-col
                xs="12"
                sm="10"
                md="8"
                id="cardTextCol"
                :style="{ fontSize: fontSize * 0.7 + 'px' }"
              >
                {{ project.content }}
              </v-col>
            </v-row>
            <v-col cols="12" id="techStack">
              <h2>Tech Stack</h2>
              <v-row id="techStackLogos">
                <v-col
                  xs="6"
                  sm="6"
                  md="3"
                  v-for="tech in project.techStack"
                  :key="tech.title"
                >
                  <img :src="tech.img" :alt="tech.alt" height="50px" />
                  <p>{{ tech.title }}</p>
                </v-col>
              </v-row>
              <v-spacer id="spacer"></v-spacer>
              <v-card-actions class="justify-center" id="cardActions">
                <nuxt-link :to="project.buttons[0].route">
                  <v-btn text outlined>{{ project.buttons[0].title }}</v-btn>
                </nuxt-link>
                <v-btn text :href="project.buttons[1].route" target="_blank">{{
                  project.buttons[1].title
                }}</v-btn>
              </v-card-actions>
            </v-col>
          </v-card-text>
        </v-col>

        <v-col xs="12" sm="6" md="6" id="inlayColumn" v-if="!showLeft(index)">
          <v-card :color="project.color" id="inlayCard" height="100%">
            <v-container fluid fill-height>
              <v-col cols="12">
                <v-img
                  :src="project.image"
                  class="inlayImage"
                  id="ttbInlayImage"
                ></v-img>
              </v-col>
            </v-container>
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      projects: [],
    }
  },
  mounted() {
    fetch('projects.json')
      .then((r) => r.json())
      .then((json) => {
        this.projects = json
      })
    console.log(this.projects)
  },
  computed: {
    fontSize() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return 18
        case 'sm':
          return 17
        case 'md':
          return 22
        case 'lg':
          return 26
        case 'xl':
          return 30
      }
    },
  },
  methods: {
    showLeft(index) {
      if (!(index % 2) || ['xs'].includes(this.$vuetify.breakpoint.name)) {
        return true
      } else {
        return false
      }
    },
  },
}
</script>

<style lang="sass" scoped>
#greatCard
  border-radius: 30px
  margin-bottom: 200px
  padding: 0
  cursor: default !important

#inlayColumn
  padding: 0

#inlayCard
  border-radius: 30px

#inlayImage
  border-radius: 0px
  max-width: 70%
  max-height: 70%
  margin: auto

.projectCardTitle
  font-weight: 600

#cardTextCol
  margin: auto

#spacer
  height: 100%

#techStack
  margin-top: 50px

#cardActions
  margin-top: 50px

#techStackLogos
  margin-top: 30px
</style>