<template>
  <div style="overflow: hidden; width: 100%">
    <v-container>
      <v-row justify="center" align="center">
        <v-row style="margin-top: 10%; width: 100%">
          <v-col cols="12" sm="8" md="7">
            <div class="landing-title">Redefining Money.</div>
          </v-col>
        </v-row>
        <v-row style="width: 100%">
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
        <v-row style="width: 100px">
          <v-btn
            @click="openLink(buildLink)"
            elevation="2"
            raised
            x-large
            style="margin-right: 10px"
            >Start Building</v-btn
          ><v-btn @click="openLink(docsLink)" elevation="2" raised x-large
            >Read The Docs</v-btn
          >
        </v-row>
      </v-row>
    </v-container>
    <img
      class="center-wolfram wolfram-bg"
      alt="Wolfram Web"
      src="wolfram/wave.svg"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      buildLink: 'https://github.com/spruce-solutions',
      docsLink: 'https://app.gitbook.com/@quai/s/quai/',
    }
  },
  methods: {
    openLink(link) {
      window.open(link, '_blank')
    },
  },
}
</script>

<style scoped>
.landing-title {
  background: linear-gradient(120deg, #ec4d37ff, #ffa500);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  opacity: 2 !important;
  color: rgba(255, 255, 255, 1) !important;
  pointer-events: none;
}

.wolfram-bg {
  position: absolute;
  /* background by SVGBackgrounds.com */
  top: 0;
  -webkit-mask-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0),
    rgba(0, 0, 0, 1)
  );
  pointer-events: none;
  display: block;
  margin-left: 20%;
  margin-right: auto;
  height: 800px;
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
    font-size: 80px;
  }
}
</style>
