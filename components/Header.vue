<template>
  <v-app-bar
    hide-on-scroll
    fixed
    app
    style="background-color: rgba(0, 0, 0, 0.2); max-width: 100vw !important"
  >
    <LogosQuaiRound style="cursor: pointer" />
    <div
      style="
        margin-left: 24%;
        margin-right: 30%;
        width: 40%;
        display: flex;
        justify-content: space-around;
      "
    >
      <v-btn
        class="header-text"
        color="white"
        text
        rounded
        nuxt
        to="/#features"
      >
        Features
      </v-btn>
      <v-btn class="header-text" color="white" text rounded nuxt to="/#roadmap">
        Roadmap
      </v-btn>
      <v-btn
        class="header-text"
        color="white"
        text
        rounded
        @click="openLink('https://medium.com/quai-network')"
      >
        News
      </v-btn>
      <v-btn
        class="header-text"
        color="white"
        text
        rounded
        @click="openLink('https://docs.quai.network/')"
      >
        Developers
      </v-btn>
      <v-btn class="header-text" color="white" text rounded nuxt to="/faq">
        FAQ
      </v-btn>
    </div>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    openLink(link) {
      window.open(link, '_blank')
    },
  },
}
</script>

<style>
@media (max-width: 700px) {
  .header-text {
    font-size: 10px !important;
  }

  .v-btn:not(.v-btn--round).v-size--default {
    padding-left: 2px;
    padding-right: 2px;
  }
}
</style>
