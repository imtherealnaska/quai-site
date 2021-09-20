<template>
  <v-app-bar
    hide-on-scroll
    fixed
    app
    style="background-color: rgba(0, 0, 0, 0.2); max-width: 100vw"
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
      <v-btn class="header-text" color="white" text rounded> Home </v-btn>
      <v-btn class="header-text" color="white" text rounded> News </v-btn>
      <v-btn class="header-text" color="white" text rounded> Developers </v-btn>
    </div>
  </v-app-bar>
</template>

<script>
export default {}
</script>

<style>
@media (max-width: 700px) {
  .header-text {
    font-size: 12px !important;
  }
}
</style>
