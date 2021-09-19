<template>
  <v-app-bar
    hide-on-scroll
    fixed
    app
    style="background-color: rgba(0, 0, 0, 0.2)"
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
      <v-btn color="white" text rounded> Home </v-btn>
      <v-btn color="white" text rounded> News </v-btn>
      <v-btn color="white" text rounded> Developers </v-btn>
      <v-btn v-if="this.now" class="countdown-btn"
        >Testnet Launch {{ display.days }} Days {{ display.hours }} Hours
        {{ display.seconds }} Seconds</v-btn
      >
    </div>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      now: null,
      end: new Date('October 14, 2021 15:00:00'),
      tick: null,
    }
  },
  watch: {
    now() {
      if (this.finished) {
        clearInterval(this.tick)
      }
    },
  },
  computed: {
    remaining() {
      return this.end.diff(this.now).toObject()
    },
    display() {
      var seconds = Math.floor((this.end - this.now) / 1000)
      var minutes = Math.floor(seconds / 60)
      var hours = Math.floor(minutes / 60)
      var days = Math.floor(hours / 24)

      hours = hours - days * 24
      minutes = minutes - days * 24 * 60 - hours * 60
      seconds = seconds - days * 24 * 60 * 60 - hours * 60 * 60 - minutes * 60
      return { days: days, hours: hours, seconds: seconds }
    },
    finished() {
      return this.now >= this.end
    },
  },
  mounted() {
    this.tick = setInterval(() => {
      this.now = new Date()
    }, 1000)
  },
}
</script>

<style>
.countdown-btn {
  background-color: rgb(236, 77, 55, 0.5) !important;
  position: absolute;
  right: 10px;
  top: 15px;
}
</style>
