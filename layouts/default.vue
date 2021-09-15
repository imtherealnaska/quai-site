<template>
  <v-app dark>
    <v-app-bar fixed app style="background-color: rgba(0, 0, 0, 0.2)">
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
        <v-btn icon> Home </v-btn>
        <v-btn icon> News </v-btn>
        <v-btn icon> Developers </v-btn>
      </div>
    </v-app-bar>
    <v-main class="background">
      <Nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>

<style>
.background {
  /* background-image: url('./static/rose-petals.svg'); */
  background-size: cover;
  background-attachment: fixed;
  background-repeat: no-repeat;
  display: table-cell !important;
  /* background by SVGBackgrounds.com */
}
</style>
