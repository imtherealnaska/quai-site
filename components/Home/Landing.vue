<template>
  <div style="width: 100%; height: 100%; overflow-x: hidden">
    <v-container>
      <v-row class="landing-row" justify="center" align="center">
        <v-col cols="12" sm="8" md="7">
          <v-row style="margin-top: 10%; width: 100%">
            <div class="landing-title">Redefining Money.</div>
          </v-row>
          <v-row class="landing-desc" style="width: 100%; height: 100%">
            Quai is a scalable network of Merged Mined blockchains enabling fast
            and inexpensive decentralized finance.
          </v-row>
          <v-row class="landing-btn-row">
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
        </v-col>
        <v-col v-if="this.now" class="countdown-col">
          <v-row class="countdown-title">Testnet Launch</v-row>
          <v-row class="countdown-nums">
            <v-btn
              @click="openLink(docsLink)"
              class="countdown-btn"
              raised
              elevantion="2"
              >{{ display.days }} Days {{ display.hours }} Hours
              {{ display.seconds }} Seconds</v-btn
            >
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      buildLink: 'https://github.com/spruce-solutions',
      docsLink: 'https://docs.quai.network/',
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
.countdown-col {
  justify-content: center;
  margin: 0 auto;
  max-width: max-content;
}

.countdown-title {
  font-size: 64px;
  position: relative;
  text-align: center;
  font-weight: 600;
  pointer-events: none;
  margin: 0 auto;
  background: linear-gradient(120deg, #ffa600, white);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.countdown-nums {
  font-size: 40px;
  position: relative;
  text-align: center;
  font-weight: 600;
}

.countdown-btn {
  background-color: rgb(236, 77, 55, 0.9) !important;
  /* background: linear-gradient(120deg, #ffa600, white); */
  font-size: 22px;
  margin: 0 auto;
  width: 100%;
}

.landing-row {
  height: 100%;
}

.landing-btn-row {
  position: relative;
  margin-top: 40px;
  width: 100%;
  height: 100%;
}

.landing-title {
  background: linear-gradient(120deg, #ec4d37ff, #ffa500);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  opacity: 2 !important;
  color: rgba(255, 255, 255, 1) !important;
  position: relative;
  pointer-events: none;
}

.landing-desc {
  position: relative;
  pointer-events: none;
}

.landing-btn {
  background-color: rgb(236, 77, 55, 0.9) !important;
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

  .countdown-btn {
    font-size: 22px;
  }
}

/* Landscape phones and portrait tablets */
@media (max-width: 767px) {
  .landing-title {
    font-size: 80px;
  }

  .countdown-btn {
    font-size: 22px;
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

  .countdown-btn {
    font-size: 22px;
  }
}

/* Portrait phones and smaller */
@media (max-width: 420px) {
  .landing-title {
    font-size: 55px;
  }

  .landing-desc {
    font-size: 20px;
  }

  .landing-row {
    margin: 10%;
  }

  .v-btn {
    font-size: 10px !important;
    padding: 0 10px !important;
  }

  .countdown-btn {
    font-size: 14px;
  }

  .countdown-title {
    font-size: 32px;
    position: relative;
    text-align: center;
    font-weight: 300;
    margin: 0 auto;
  }
}
</style>
