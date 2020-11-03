<template>
  <article>
    <v-row justify="center" id="articleTitle">
      <h1>{{ page.title }}</h1>
    </v-row>
    <v-row justify="center" id="description">
      <p>{{ page.description }}</p>
    </v-row>
    <v-row justify="center">
      <v-col xs="12" sm="10" md="8" lg="6">
        <v-card id="imageCard">
          <v-img :src="page.img"></v-img>
        </v-card>
      </v-col>
    </v-row>
    <v-row justify="center" id="contentRow">
      <v-col xs="12" sm="10" md="8">
        <v-card>
          <v-row justify="center">
            <v-col cols="10">
              <nuxt-content id="content" :document="page" />
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params, error }) {
    const slug = params.slug || 'index'
    const page = await $content('projects', slug)
      .fetch()
      .catch((err) => {
        error({ statusCode: 404, message: 'Page not found' })
      })

    return {
      page,
    }
  },
}
</script>

<style lang="sass" scoped>
#description
  margin-bottom: 20px

#contentRow
  // width: 80%
  margin-left: auto
  margin-right: auto

#content
  padding: 2rem

#imageCard
  // width: 30%
  border-radius: 15px
  margin-bottom: 20px

#articleTitle
  margin-top: 50px
</style>