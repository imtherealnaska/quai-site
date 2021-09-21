<template>
  <v-app-bar
    hide-on-scroll
    fixed
    app
    style="background-color: rgba(0, 0, 0, 0.2); max-width: 100vw !important"
  >
    <LogosQuaiRound />
    <div
      style="
        margin-left: 24%;
        margin-right: 30%;
        width: 40%;
        display: flex;
        justify-content: space-around;
      "
    >
      <v-menu open-on-hover offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            class="header-text"
            color="white"
            text
            rounded
            v-on="on"
            v-bind="attrs"
            nuxt
            to="/"
          >
            Home
          </v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
            :to="{ path: '/', hash: '#' + item.id }"
          >
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
      <v-btn
        class="header-text"
        color="white"
        text
        rounded
        :to="{ path: '/faq' }"
      >
        FAQs
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
        @click="openLink('https://app.gitbook.com/@quai/s/quai/')"
      >
        Developers
      </v-btn>
    </div>
  </v-app-bar>
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: 'Features', id: 'features' },
      { title: 'About', id: 'about' },
      { title: 'Roadmap', id: 'roadmap' },
    ],
  }),
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
    font-size: 12px !important;
  }
}
</style>
