<template>
  <div style="overflow: hidden; padding-bottom: 10%">
    <div class="merged-mining-bg"></div>
    <v-container id="card1" class="card-color-3">
      <v-card-text style="position: relative">
        <h1 class="text-h1 gradient-text gradient-text-3">
          Decentralized Bridges: Trustless Cross-Chain Value Transfers
        </h1>
        <div class="text--primary" style="pointer-events: none">
          Janus governs the transfer of value within and across the Quai
          Network.<br /><br />
        </div>
        <div class="body-text-desc">
          The Quai Network utilizes coincident blocks created from merged mining
          to transfer state across blockchains. As a lower blockchain's security
          is validated in the Prime blockchain, hashlinks become available to be
          traced and transferred.
        </div>
      </v-card-text>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'The Merged Mined Network of Blockchains | Decentralized Bridges',
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'Decentralized Bridges',
          name: 'Decentralized Bridges',
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
  background-image: url('./static/wolfram/leaves.png');
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

.card-color-3 {
  margin-top: 10%;
  border-radius: 20px;
  -webkit-box-shadow: 0 0 20px #57dd0a !important;
  -moz-box-shadow: 0 0 20px #57dd0a !important;
  box-shadow: 0 0 20px #57dd0a !important;
}

.gradient-text {
  line-height: 5.5rem;
  font-size: 5rem !important;
  pointer-events: none;
}

.gradient-text-3 {
  background: linear-gradient(#57dd0a, rgb(55, 133, 236));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

@media (max-width: 900px) {
  .body-text-desc {
    font-size: 14px !important;
  }
  .gradient-text-features {
    font-size: 3rem !important;
  }

  .gradient-text {
    line-height: 5.5rem;
    font-size: 3rem !important;
  }
}
</style>
