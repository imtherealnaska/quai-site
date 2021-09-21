<template>
  <div style="height: 100%">
    <v-container class="about-container">
      <v-row style="margin-top: 10%; width: 100%">
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
          <v-row style="font-size: 24px"
            >The creators of Quai believe in a future where Proof of Work is
            scalable. That is why Quai is built with a multi-chain approach to
            scalability. Quai’s unique network of blockchains allows for
            seamless interaction across chains while maintaining
            decentralization. Quai is also EVM compatible, so bringing over your
            favorite DeFi protocols or NFT projects is a breeze.
          </v-row>
        </v-col>
        <v-col cols="12" sm="12" md="6">
          <v-row style="font-size: 100px">
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
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <v-btn
      elevation="2"
      raised
      x-large
      style="margin-top: 200px; display: flex; margin: 0 auto"
      >Read The Whitepaper</v-btn
    >
  </div>
</template>

<script>
export default {
  mounted() {
    var vid = document.getElementById('video')
    if (vid != null) {
      vid.playbackRate = 1.4
    }
  },
}
</script>

<style scoped>
.animation {
  margin: 20%;
  width: 100%;
  border-radius: 20px;
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

@media (max-width: 900px) {
  .about-container {
    margin: 5%;
  }

  .animation {
    margin-top: 60px;
    margin-left: 0;
    width: 100%;
    border-radius: 20px;
  }

  .about-text-1 {
    font-size: 60px;
  }

  .about-text-2 {
    font-size: 60px;
  }

  .about-text-3 {
    font-size: 60px;
  }
}
</style>
