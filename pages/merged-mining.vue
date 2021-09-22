<template>
  <div style="overflow: hidden; padding-bottom: 10%">
    <div class="merged-mining-bg"></div>
    <v-container id="card1" class="card-color-1">
      <v-card-text style="position: relative">
        <h1 class="text-h1 gradient-text gradient-text-1">
          Merged Mining: Sharing Hashrate Across Blockchains
        </h1>
        <div class="text--primary" style="pointer-events: none">
          Hermes controlls the organization and structure of the Quai Network,
          dictating it's shape and form.<br /><br />
        </div>
        <div class="body-text-desc">
          Merged Mining utilizes hashrate across multiple blockchains. In many
          cases, these disparate blockchains do not share the same incentives or
          utilize the true power of merged mining. The Quai Network shares
          headers of hierarchical chains in a way that creates verifiable and
          trusted links. Quai initially will take the form of a 3x3 pyramid. Our
          roadmap contains flexible hierarchies as demand fluctuates for the
          network.
        </div>
      </v-card-text>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'The Merged Mined Network of Blockchains | Merged Mining',
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'Merged Mining',
          name: 'Merged Mining',
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
  width: 50vw;
  height: 98vh;
  background: transparent;
  background-image: url('./static/wolfram/mesh.png');
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

.card-color-1 {
  margin-top: 10%;
  border-radius: 20px;
  -webkit-box-shadow: 0 0 20px#dda50a !important;
  -moz-box-shadow: 0 0 20px #dda50a !important;
  box-shadow: 0 0 20px #dda50a !important;
}

.wolfram-bg-1 {
  background-image: url('./static/wolfram/mesh.png');
}

.gradient-text {
  line-height: 5.5rem;
  font-size: 5rem !important;
  pointer-events: none;
}

.gradient-text-1 {
  background: linear-gradient(150deg, #dda50a, #ec4d37ff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

@media (max-width: 900px) {
  .body-text-desc {
    font-size: 14px !important;
  }

  .gradient-text {
    line-height: 5.5rem;
    font-size: 3rem !important;
  }
}
</style>
