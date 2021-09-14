<template>
  <v-footer dark padless class="footer-style">
    <v-card
      flat
      tile
      class="lighten-1 white--text text-center"
      style="border-radius: 25px !important"
    >
      <v-card-text>
        <v-btn v-for="icon in icons" :key="icon" class="mx-1 white--text" icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: ['mdi-facebook', 'mdi-twitter', 'mdi-linkedin', 'mdi-instagram'],
  }),
}
</script>

<style scoped>
.footer-style {
  position: fixed;
  bottom: 10px;
  right: 10px;
  background: none;
}
</style>
