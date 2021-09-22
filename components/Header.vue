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
          <v-list-item v-for="(item, index) in home" :key="index" :to="item.to">
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
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
            to="/design"
          >
            Protocol Design
          </v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, index) in design"
            :key="index"
            :to="item.to"
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
    </div>
  </v-app-bar>
</template>

<script>
export default {
  data: () => ({
    home: [
      { title: 'Features', to: { path: '/', hash: '#features' } },
      { title: 'About', to: { path: '/', hash: '#about' } },
      { title: 'Roadmap', to: { path: '/', hash: '#roadmap' } },
    ],
    design: [
      { title: 'Hermes: Merged Mining', to: { path: '/merged-mining' } },
      { title: 'Janus: Decentralizd Bridges', to: { path: '/bridges' } },
      { title: 'Plutus: Tokenomics', to: { path: '/tokenomics' } },
      { title: 'Ares: Incentives', to: { path: '/incentives' } },
      { title: 'FAQs', to: { path: '/faq' } },
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
    font-size: 10px !important;
  }

  .v-btn:not(.v-btn--round).v-size--default {
    padding-left: 2px;
    padding-right: 2px;
  }
}
</style>
