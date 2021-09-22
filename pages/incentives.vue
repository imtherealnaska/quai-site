<template>
  <div style="overflow: hidden; padding-bottom: 10%">
    <div class="merged-mining-bg"></div>
    <v-container id="card1" class="card-color-4">
      <v-card-text style="position: relative">
        <h1 class="text-h1 gradient-text gradient-text-4">
          Incentives: Using Blockchain Utility for Value Creation
        </h1>
        <div class="text--primary" style="pointer-events: none">
          Ares dictates incentives that drive growth on the Quai Network.<br /><br />
        </div>
        <div class="body-text-desc">
          Quai will employ not only merged mining within its own network but
          also to other blockchain platforms in order to co-op hashrate. This
          will allow Quai to bootstrap hashrate.
          <br />
          Other incentives will exist in the future for Quai users such as
          airdrops from snapshotted Bitcoin and Ethereum state.
        </div>
      </v-card-text>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'The Merged Mined Network of Blockchains | Incentives',
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'Incentives',
          name: 'Incentives',
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
  background-image: url('./static/wolfram/web.png');
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

.card-color-4 {
  margin-top: 10%;
  border-radius: 20px;
  -webkit-box-shadow: 0 0 20px #9a0add !important;
  -moz-box-shadow: 0 0 20px #9a0add !important;
  box-shadow: 0 0 20px #9a0add !important;
}

.gradient-text {
  line-height: 5.5rem;
  font-size: 5rem !important;
  pointer-events: none;
}

.gradient-text-4 {
  background: linear-gradient(160deg, #9a0add, rgb(236, 55, 55));
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
