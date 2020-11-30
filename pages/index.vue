<template>
  <v-container fill-height fluid>
    <v-row justify="center" align="center" id="home">
      <v-card
        class="techCard hidden-sm-and-down animate__animated animate__bounce"
        rounded
        id="vuetifyCard"
        hover
        v-anime="{
          translateY: 100,
          opacity: 1,
          duration: 2000,
          delay: 1000,
          loop: false,
        }"
      >
        <v-row class="techCardRow">
          <img
            src="vuetify-logo.svg"
            alt="Vuetify"
            height="50px"
            class="techCardImage"
          />
          <h1>Vuetify</h1>
        </v-row>
      </v-card>
      <v-card
        class="techCard hidden-sm-and-down"
        rounded
        id="vueCard"
        hover
        v-anime="{
          translateY: 100,
          opacity: 1,
          duration: 2000,
          delay: 1000,
          loop: false,
        }"
      >
        <v-row class="techCardRow">
          <img
            src="vueLogo.jpeg"
            alt="Vue"
            height="50px"
            class="techCardImage"
          />
          <h1>Vue.js</h1>
        </v-row>
      </v-card>
      <v-card
        class="techCard hidden-sm-and-down"
        rounded
        id="firebaseCard"
        hover
        v-anime="{
          translateY: 100,
          opacity: 1,
          duration: 2000,
          delay: 1000,
          loop: false,
        }"
      >
        <v-row class="techCardRow">
          <img
            src="firebaseLogo.png"
            alt="Firebase"
            height="50px"
            class="techCardImage"
          />
          <h1>Firebase</h1>
        </v-row>
      </v-card>
      <v-card
        class="techCard hidden-sm-and-down"
        rounded
        id="nuxtCard"
        hover
        v-anime="{
          translateY: 100,
          opacity: 1,
          duration: 2000,
          delay: 1000,
          loop: false,
        }"
      >
        <v-row class="techCardRow">
          <img
            src="nuxtjs.png"
            alt="Nuxt.js"
            height="50px"
            class="techCardImage"
          />
          <h1>Nuxt.js</h1>
        </v-row>
      </v-card>
      <v-card
        class="techCard hidden-sm-and-down"
        rounded
        id="netlifyCard"
        hover
        v-anime="{
          translateY: 100,
          opacity: 1,
          duration: 2000,
          delay: 1000,
          loop: false,
        }"
      >
        <v-row class="techCardRow">
          <img
            src="netlifyLogo.png"
            alt="Nuxt.js"
            height="50px"
            class="techCardImage"
          />
          <h1>Netlify</h1>
        </v-row>
      </v-card>
      <v-col
        cols="12"
        xs="12"
        sm="6"
        md="6"
        v-anime="{
          translateY: 100,
          opacity: 1,
          duration: 2000,
          delay: 1000,
          loop: false,
        }"
        id="introText"
      >
        <v-row justify="center" class="text-center">
          <v-col cols="12">
            <h1 id="mainTitle">Hey there!</h1>
            <h2 id="subTitle">I'm Thaeke, and I'm a front-end developer.</h2>
            <v-btn
              text
              large
              id="learnMore"
              v-scroll-to="{ el: '#work', offset: -100 }"
            >
              Check Out My Work
            </v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-row>

    <!-- My Work Title -->
    <v-row
      justify="center"
      id="workTitle"
      :style="{
        marginTop: this.$vuetify.breakpoint.xs ? '20vh' : '40vh',
        marginBottom: '30px',
      }"
    >
      <h1 v-anime="{
          translateY: 100,
          opacity: 1,
          duration: 2000,
          delay: 1000,
          loop: false,
        }" id="work">My Work</h1>
    </v-row>

    <v-row justify="center" align="center">
      <v-col xs="12" sm="12" md="10" lg="8" id="itemColumn">
        <!-- Projects -->
        <project-card></project-card>

        <!-- About Me Title -->
        <v-row justify="center" id="aboutTitle">
          <h1 id="about">About Me</h1>
        </v-row>
        <v-row justify="center">
          <v-col xs="6" sm="10" md="12" lg="10">
            <v-card>
              <v-card-title class="justify-center"> Who am I? </v-card-title>
              <v-card-text class="text-center">
                <v-avatar size="300px" id="avatar">
                  <v-img src="profilepicture.jpg"></v-img>
                </v-avatar>
                <p id="aboutMeParagraph">
                  Hey there! My name is Thaeke, and I’m from the Netherlands.<br />
                  I was born in 1997 on a farm in the Noordoostpolder. <br />
                  I’m obsessed with learning from a broad variety of subjects.
                  <br /><br />
                  My main passions are the environment, computer science and
                  software development, philosophy, and psychology. <br />
                  I am doing a parttime Bachelor in Environmental Sciences at
                  the Open University in the Netherlands.<br /><br />
                  Creating things and coming up with new projects to work on is
                  something I thoroughly enjoy.<br />
                  Which is one of the reasons I have started developing as a
                  front-end web developer.<br /><br />
                  Three years ago, I started learning HTML and CSS, and started
                  making some WordPress websites.<br />
                  Then I started seeing the necessity of JavaScript and some of
                  its frameworks for quality front-end web development.<br />
                  While I started learning vanilla JavaScript, I was looking
                  forward to learning some of the JS frameworks.<br /><br />
                  After making some things with JS, and solving a bunch of
                  problems on Code Academy, I was finally ready to learn a JS
                  framework.<br />
                  I chose Vue.js as my first JS framework because it seemed very
                  powerful and had a short learning curve.<br />
                  This meant I could start playing around and building my own
                  apps.<br />
                  I've learned a lot in the last years, and I'm excited to learn
                  more! <br />
                  <br />
                  <strong>You can find me on the following platforms:</strong>
                </p>
              </v-card-text>
              <v-card-actions>
                <v-row justify="center">
                  <v-col cols="6">
                    <social-link></social-link>
                  </v-col>
                </v-row>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
        <v-row justify="center" id="contactTitle">
          <h1 id="contact">Contact Me</h1>
        </v-row>
        <v-row justify="center">
          <v-col xs="8" sm="10" md="12" lg="10">
            <v-card>
              <v-card-title>
                <h2 id="contactFormTitle">Send me a message!</h2>
              </v-card-title>
              <v-row justify="center">
                <v-col xs="8" sm="8" md="6">
                  <v-form
                    id="contactForm"
                    ref="form"
                    @submit.prevent="sendEmail"
                  >
                    <v-text-field
                      name="name"
                      label="Name"
                      v-model="name"
                      color="secondary"
                      :rules="nameRules"
                    ></v-text-field>
                    <v-text-field
                      name="email"
                      label="Email"
                      v-model="email"
                      color="secondary"
                      :rules="emailRules"
                    ></v-text-field>
                    <v-textarea
                      name="message"
                      label="Message"
                      v-model="message"
                      color="secondary"
                      :rules="messageRules"
                    ></v-textarea>
                    <v-card-actions class="justify-center">
                      <v-btn
                        text
                        type="submit"
                        value="Send"
                        :loading="loading"
                        :disabled="loading"
                      >
                        Send
                        <v-icon right> mdi-send </v-icon>
                      </v-btn>
                    </v-card-actions>
                  </v-form>
                  <form></form>
                </v-col>
              </v-row>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-snackbar v-model="snackbar" top color="success">
      <span id="snackbarContent"
        >Thank you for your message! I'll be in contact soon!</span
      >
    </v-snackbar>
  </v-container>
</template>

<script>
import emailjs from 'emailjs-com'
import ProjectCard from '@/components/ProjectCard'
import SocialLink from '@/components/SocialLink'

export default {
  head: {
    title: 'Portfolio',
  },
  data() {
    return {
      name: '',
      email: '',
      message: '',
      loading: false,
      snackbar: false,
      nameRules: [
        (v) => !!v || 'Name is required',
        (v) => v.length <= 25 || 'Name must be less than 25 characters',
      ],
      messageRules: [(v) => !!v || 'Message is required'],
      emailRules: [
        (v) => !!v || 'E-mail is required',
        (v) => /.+@.+/.test(v) || 'E-mail must be valid',
      ],
      projectList: [],
    }
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
    smallScreen() {
      if (this.$vuetify.breakpoint.name == 'xs') {
        return true
      }
    },
  },
  methods: {
    goTo(goal) {
      if (!this.$route.params.slug) {
        this.$router.push('#' + goal)
      } else {
        this.$router.push({ path: `/#${goal}` })
      }
      this.drawer = false
    },
    sendEmail(e) {
      if (this.$refs.form.validate()) {
        try {
          emailjs.sendForm(
            'service_duzp5pe',
            'template_qkbktna',
            e.target,
            'user_HkCjUmtgKD8JTx2Jgqkux',
            {
              name: this.name,
              email: this.email,
              message: this.message,
            }
          )
          this.setLoader()
          // Reset form field
          this.name = ''
          this.email = ''
          this.message = ''
          this.$refs.form.resetValidation()
        } catch (error) {}
      }
    },
    setLoader() {
      var self = this
      this.loading = true
      setTimeout(function () {
        self.loading = false
        self.snackbar = true
      }, 2000)
    },
  },
}
</script>

<style lang="sass" scoped>
.bounceInUp-enter-active
  animation: bounceInUp .8s

.bounceInUp-leave-active
  animation: bounceInUp .5s

#home
  margin-top: 15vh

#mainTitle
  font-size: 3rem
  font-weight: 500

#subTitle
  font-size: 2rem
  font-weight: 400

#learnMore
  margin-top: 40px

#outlinedButtonText
  font-size: 1.5rem
  padding-top: 50px

#introCard
  border-radius: 50px

#introText
  opacity: 0

.hoverCard
  transition: opacity .4s ease-in-out

#hoverCard
  border-radius: 20px
  cursor: pointer

#greatCard
  border-radius: 30px
  margin-bottom: 200px
  padding: 0
  cursor: default !important

#itemColumn
  padding: 0

#inlayColumn
  padding: 0

#inlayCard
  border-radius: 30px

.inlayImage
  border-radius: 30px
  margin-top: auto
  margin-bottom: auto

#uiInlayImage
  max-width: 60%
  margin-left: auto
  margin-right: auto
  border-radius: 0

#cardTextCol
  margin: auto

.underlinedBottom
  text-decoration: underline

#aboutTitle
  margin-top: 100px

.techCard
  position: absolute
  display: flex
  cursor: default !important

.techCardRow
  padding: 20px 30px 20px 30px

.techCardImage
  margin-right: 30px

#firebaseCard
  top: 35vh
  opacity: 0
  @media (max-width: 1400px)
    left: 2vw
  @media (min-width: 1400px)
    left: 10vw

#netlifyCard
  right: 10vw
  top: 35vh
  opacity: 0
  @media (max-width: 1400px)
    right: 2vw
  @media (min-width: 1400px)
    right: 10vw

#vuetifyCard
  top: 50vh
  opacity: 0
  @media (max-width: 1400px)
    left: 17vw
  @media (min-width: 1400px)
    left: 25vw

#nuxtCard
  right: 25vw
  top: 50vh
  opacity: 0
  @media (max-width: 1400px)
    right: 17vw
  @media (min-width: 1400px)
    right: 25vw

#vueCard
  top: 65vh
  opacity: 0

#work
  margin-top: 150px

#about
  margin-top: 160px

#contact
  margin-top: 160px

.projectCardTitle
  font-weight: 600

#contactFormTitle
  margin-left: auto
  margin-right: auto
  font-size: 24px

#aboutMeParagraph
  font-size: 16px

#avatar
  margin-bottom: 30px

#snackbarContent
  color: white
  font-weight: 500
  font-size: 18px
</style>