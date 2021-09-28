<template>
  <div class="about-section">
    <v-container>
      <v-row class="about-container" style="width: 100%">
        <v-col cols="12" sm="6" md="6">
          <v-row style="font-size: 74px">
            <div class="about-text-1">Fast.</div>
          </v-row>
          <v-row style="font-size: 74px">
            <div class="about-text-2">Secure.</div>
          </v-row>
          <v-row style="font-size: 74px">
            <div class="about-text-3">Decentralized.</div>
          </v-row>
          <v-row class="about-desc"
            >Quai’s unique network of blockchains allows for seamless
            interaction across chains while maintaining decentralization. Quai
            is EVM compatible, so migrating your favorite DeFi protocols or NFT
            projects is a breeze.
          </v-row>
        </v-col>
        <v-col
          cols="12"
          sm="12"
          md="6"
          style="display: flex; justify-content: center; align-items: center"
        >
          <video
            class="animation"
            muted
            autoplay
            loop
            playsinline
            defaultMuted
            style="max-width: 100%"
            id="video"
          >
            <source src="~/assets/animation.mp4" type="video/mp4" />
            Your browser does not support the video tag.
          </video>
        </v-col>
      </v-row>
    </v-container>
    <v-btn
      elevation="2"
      raised
      x-large
      style="
        display: flex;
        margin: 0 auto;
        margin-top: 100px;
        background-color: rgb(236, 77, 55, 0.9);
        pointer-events: all;
      "
      target="_blank"
      @click="openLink('https://arxiv.org/abs/1811.00125')"
      >Read The Whitepaper</v-btn
    >
  </div>
</template>

<script>
export default {
  mounted() {
    var vid = document.getElementById('video')
    if (vid != null) {
      vid.playbackRate = 1.2
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
.about-section {
  pointer-events: none;
}

.animation {
  width: 95%;
  border-radius: 20px;
  -webkit-box-shadow: 0 0 20px white;
  -moz-box-shadow: 0 0 20px white;
  box-shadow: 0 0 20px white;
}

.about-text-1 {
  background: linear-gradient(120deg, yellow, #ffa500);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-right: 20px;
}

.about-text-2 {
  background: linear-gradient(120deg, white, grey);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-right: 20px;
}

.about-text-3 {
  background: linear-gradient(120deg, aqua, #57dd0a);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-right: 20px;
}

.about-desc {
  font-size: 24px;
}

@media (max-width: 900px) {
  .about-container {
    margin-left: 2%;
    margin-right: 2%;
  }

  .about-text-1 {
    font-size: 40px;
  }

  .about-text-2 {
    font-size: 40px;
  }

  .about-text-3 {
    font-size: 40px;
  }

  .about-desc {
    font-size: 14px;
  }
}
</style>
