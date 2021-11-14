<template>
  <div style="overflow: hidden; padding-bottom: 10%">
    <div class="merged-mining-bg"></div>
    <v-container id="card1" class="card-color-2">
      <v-card-text style="position: relative">
        <h3 class="text-h1 gradient-text gradient-text-2">
          Tokenomics: Governing The Flow of Money
        </h3>
        <div class="text--primary" style="pointer-events: none">
          Plutus governs the creation and flow of value on the Quai Network.<br /><br />
        </div>
        <div class="body-text-desc">
          Quai employs immensly powerful tokenomics that encourse users, miners,
          and developers to use the Quai Network. As miners secure parts of the
          network, they will mine what is called a "slice". A slice of the Quai
          Network pertains to validating the Prime blockchain, a single Region
          blockchain, and a single Zone blockchain that comes from the mined
          Region blockchain. Each of these blockchains releases $QUAI as reward
          proportionally to the overall security of the network. <br />
          Users will be able to choose which blockchain they interact in based
          off a security and speed trade-off. Interacting in Prime will be the
          closest to interacting with Bitcoin and Ethereum as we know it and
          will provide similar security. Interacting in a Zone will provide
          immensly faster finality times at the cost of potentially lesser
          hashrate securing the chain.
        </div>
      </v-card-text>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'The Merged Mined Network of Blockchains | Tokenomics',
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'Tokenomics',
          name: 'Tokenomics',
          content:
            'Quai is a scalable network of blockchains designed for the future. Visit our site to learn more!',
        },
      ],
    }
  },
}
</script>

<style scoped>
.merged-mining-bg {
  width: 75vw;
  height: 98vh;
  background: transparent;
  background-image: url('./static/wolfram/pillow.png');
  background-size: cover;
  background-repeat: no-repeat;
  -webkit-mask-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0),
    60%,
    rgba(0, 0, 0, 1)
  );
  position: absolute;
  top: 0;
  right: 0;
}

.body-text-desc {
  font-size: 20px !important;
  pointer-events: none;
}

.card-color-2 {
  margin-top: 10%;
  border-radius: 20px;
}

.gradient-text {
  line-height: 5.5rem;
  font-size: 5rem !important;
  pointer-events: none;
}

.gradient-text-2 {
  background: linear-gradient(179deg, #0addcb, rgb(103, 55, 236));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

@media (max-width: 900px) {
  .body-text-desc {
    font-size: 14px !important;
  }

  .gradient-text {
    line-height: 3rem;
    font-size: 3rem !important;
  }
}
</style>
