<template>
  <v-app dark>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="8" md="6">
        <v-card>
          <v-card-title class="headline">
            Oops you're in the wrong place!
          </v-card-title>
          <v-card-title class="headline">
            <h1 v-if="error.statusCode === 404">
              {{ pageNotFound }}
            </h1>
            <h1 v-else>
              {{ otherError }}
            </h1>
          </v-card-title>
          <v-card-text>
            <p>
              If you have questions, please join the official
              <a
                href="https://discord.gg/p6BKANkYhh"
                target="_blank"
                rel="noopener noreferrer"
                title="chat"
              >
                discord </a
              >.
            </p>
            <p>
              Find a bug? Report it on the github
              <a
                href="https://github.com/spruce-solutions/quai-site"
                target="_blank"
                rel="noopener noreferrer"
                title="contribute"
              >
                issue board </a
              >.
            </p>
          </v-card-text>
          <v-card-actions>
            <v-spacer />
            <v-btn color="primary" nuxt to="/"> Return Home </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  layout: 'empty',
  props: {
    error: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      pageNotFound: '404 Not Found',
      otherError: 'An error occurred',
    }
  },
  head() {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title,
    }
  },
}
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
