<template>
  <div style="width: 100%; height: 100%; overflow-x: hidden">
    <v-container>
      <v-row class="landing-row" justify="center" align="center">
        <v-row style="margin-top: 10%; width: 100%">
          <v-col cols="12" sm="8" md="7">
            <div class="landing-title">Redefining Money.</div>
          </v-col>
        </v-row>
        <v-row style="width: 100%; height: 100%">
          <v-col
            cols="12"
            sm="8"
            md="7"
            class="landing-desc"
            style="pointer-events: none"
            >Supercharge your blockchain experience with Quai. Quai provides the
            infrastructure for the future through a secure network of Merged
            Mined blockchains.
          </v-col>
        </v-row>
        <v-row style="width: 100%; height: 100%">
          <v-btn
            @click="openLink(buildLink)"
            class="landing-btn"
            raised
            elevantion="2"
            style="margin-right: 20px"
            >Start Building</v-btn
          ><v-btn
            @click="openLink(docsLink)"
            class="landing-btn"
            raised
            elevantion="2"
            >Read The Docs</v-btn
          >
        </v-row>
        <v-row style="margin-top: 40px; margin-bottom: 40px">
          <v-btn v-if="this.now" class="countdown-btn"
            >Testnet Launch {{ display.days }} Days {{ display.hours }} Hours
            {{ display.seconds }} Seconds</v-btn
          >
        </v-row>
      </v-row>
    </v-container>
    <div class="mask" style="width: 100vw; height: 100vh"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      buildLink: 'https://github.com/spruce-solutions',
      docsLink: 'https://app.gitbook.com/@quai/s/quai/',
      now: null,
      end: new Date('October 14, 2021 15:00:00'),
      tick: null,
    }
  },
  methods: {
    openLink(link) {
      window.open(link, '_blank')
    },
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

<style scoped>
.countdown-btn {
  background-color: rgb(236, 77, 55, 0.5) !important;
}

.landing-row {
  height: 100%;
}

.landing-title {
  background: linear-gradient(120deg, #ec4d37ff, #ffa500);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  opacity: 2 !important;
  color: rgba(255, 255, 255, 1) !important;
  /* pointer-events: none; */
}

.mask {
  height: 100%;
  background: transparent;
  background-image: url('./static/wolfram/wave.svg');
  background-size: cover;
  background-repeat: no-repeat;
  -webkit-mask-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0),
    80%,
    rgba(0, 0, 0, 1)
  );
  position: absolute;
  top: 0;
}

.landing-btn {
  background-color: rgb(236, 77, 55, 0.5) !important;
}

/* Show in Large desktops and laptops */
@media (min-width: 1200px) {
  .landing-title {
    font-size: 120px;
  }
  .landing-desc {
    font-size: 24px;
  }
}

/*Hide in Other Small Devices */

/* Landscape tablets and medium desktops */
@media (min-width: 992px) and (max-width: 1199px) {
  .landing-title {
    font-size: 80px;
  }
}

/* Portrait tablets and small desktops */
@media (min-width: 768px) and (max-width: 991px) {
  .landing-title {
    font-size: 80px;
  }
}

/* Landscape phones and portrait tablets */
@media (max-width: 767px) {
  .landing-title {
    font-size: 80px;
  }
}

/* Portrait phones and smaller */
@media (max-width: 480px) {
  .landing-title {
    font-size: 65px;
  }

  .landing-desc {
    font-size: 20px;
  }

  .landing-row {
    margin: 10%;
  }
}

/* Portrait phones and smaller */
@media (max-width: 400px) {
  .landing-title {
    font-size: 55px;
  }

  .landing-desc {
    font-size: 20px;
  }

  .landing-row {
    margin: 10%;
  }
}
</style>
