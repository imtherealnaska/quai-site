<template>
  <div class="quai-cards-wrapper">
    <div class="quai-cards">
      <div id="card1" class="quai-category-card card-color-1">
        <div class="floating-wolfram wolfram-bg-1"></div>
        <v-card-text style="position: relative">
          <p class="text-h3 gradient-text gradient-text-1">Merged Mining</p>
          <div class="body-text-desc">
            Merged Mining is a way in which miners can mine more than one chain
            at once. Quai uses this to share security over many different chains
            while optimizing for fast transactions.
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn
            text
            color="#dda50a"
            style="cursor: pointer"
            nuxt
            to="/merged-mining"
          >
            Learn More
          </v-btn>
        </v-card-actions>
      </div>
      <div id="card3" class="quai-category-card card-color-3">
        <div id="janusBg" class="floating-wolfram wolfram-bg-3"></div>
        <v-card-text style="position: relative">
          <p class="text-h3 gradient-text gradient-text-2">
            Decentralized Bridges
          </p>
          <div class="body-text-desc">
            Bridges allow for the transfer of funds across blockchains. Quai
            Network has a built in bridging system that is fully decentralized.
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="#57dd0a" nuxt to="/bridges"> Learn More </v-btn>
        </v-card-actions>
      </div>
      <div id="card2" class="quai-category-card card-color-2">
        <div class="floating-wolfram wolfram-bg-2"></div>
        <v-card-text style="position: relative">
          <p class="text-h3 gradient-text gradient-text-3">Tokenomics</p>
          <div class="body-text-desc">
            Tokenomics create value over time. Quai Network uses a longterm
            deflationary system with other unique methods for creating
            stability.
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="#0addcb" nuxt to="/tokenomics"> Learn More </v-btn>
        </v-card-actions>
      </div>
      <div id="card4" class="quai-category-card card-color-4">
        <div class="floating-wolfram wolfram-bg-4"></div>
        <v-card-text style="position: relative">
          <p class="text-h3 gradient-text gradient-text-4">Incentives</p>
          <div class="body-text-desc">
            Incentives drive adoption, read more to see how Quai has a distinct
            advantage.
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="#9a0add" nuxt to="/incentives"> Learn More </v-btn>
        </v-card-actions>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cardOneActive: false,
      cardTwoActive: false,
      cardThreeActive: false,
      cardFourActive: false,
    }
  },
  methods: {},
}
</script>

<style scoped>
.quai-cards-wrapper {
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  -webkit-box-pack: center;
  justify-content: center;
  padding: 0px 2em;
  margin-left: 10%;
  margin-right: 10%;
  margin-top: 4%;
}

.quai-cards {
  display: grid;
  grid-template-columns: repeat(2, minmax(0px, 616px));
  grid-template-rows: repeat(5, minmax(0px, 150px));
  grid-auto-rows: 1fr;
  column-gap: 5em;
  row-gap: 2.5em;
}

.quai-category-card {
  overflow: hidden !important;
  border-radius: 25px;
  position: relative;
  background-color: none !important;
  width: 100%;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  flex-direction: column;
  -webkit-box-pack: justify;
  justify-content: space-between;
  height: 300px;
}

.body-text-desc {
  font-size: 20px !important;
  pointer-events: none;
}

.card-color-1 {
  -webkit-box-shadow: 0 0 20px#dda50a !important;
  -moz-box-shadow: 0 0 20px #dda50a !important;
  box-shadow: 0 0 20px #dda50a !important;
  grid-column-start: 1;
  grid-column-end: 1;
  grid-row-start: 1;
  grid-row-end: 3;
}

.card-color-2 {
  -webkit-box-shadow: 0 0 20px #0addcb !important;
  -moz-box-shadow: 0 0 20px #0addcb !important;
  box-shadow: 0 0 20px #0addcb !important;
  grid-column-start: 1;
  grid-column-end: 1;
  grid-row-start: 3;
  grid-row-end: 5;
}
.card-color-3 {
  -webkit-box-shadow: 0 0 20px #57dd0a !important;
  -moz-box-shadow: 0 0 20px #57dd0a !important;
  box-shadow: 0 0 20px #57dd0a !important;
  grid-column-start: 2;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 3;
}
.card-color-4 {
  -webkit-box-shadow: 0 0 20px #9a0add !important;
  -moz-box-shadow: 0 0 20px #9a0add !important;
  box-shadow: 0 0 20px #9a0add !important;
  grid-column-start: 2;
  grid-column-end: 2;
  grid-row-start: 3;
  grid-row-end: 5;
}

.floating-wolfram {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background-size: cover;
  background-repeat: no-repeat;
  -webkit-mask-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0),
    rgba(0, 0, 0, 1)
  );
  -webkit-backface-visibility: hidden; /* actual workaround */
  backface-visibility: hidden; /* perhaps this is not needed */
  -webkit-transition: all 0.5s ease-in-out;
  -moz-transition: all 0.5s ease-in-out;
  -o-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
}

.wolfram-bg-1 {
  background-image: url('./static/wolfram/mesh.png');
}

.wolfram-bg-2 {
  background-image: url('./static/wolfram/pillow.png');
}
.wolfram-bg-3 {
  background-image: url('./static/wolfram/leaves.png');
}
.wolfram-bg-4 {
  background-image: url('./static/wolfram/web.png');
}

.gradient-text {
  line-height: 3.5rem;
  font-size: 3rem !important;
  pointer-events: none;
}

.gradient-text-1 {
  background: linear-gradient(150deg, #dda50a, #ec4d37ff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradient-text-2 {
  background: linear-gradient(#57dd0a, rgb(55, 133, 236));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradient-text-3 {
  background: linear-gradient(179deg, #0addcb, rgb(103, 55, 236));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradient-text-4 {
  background: linear-gradient(160deg, #9a0add, rgb(236, 55, 55));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

@media (max-width: 900px) {
  .quai-cards-wrapper {
    margin-left: 0;
    margin-right: 0;
  }
  .quai-cards {
    display: grid;
    grid-template-columns: repeat(1, minmax(0px, 616px));
    grid-template-rows: repeat(4, minmax(0px, 275px));
    grid-auto-rows: 1fr;
    gap: 2.5em;
  }

  .quai-category-card {
    height: 275px;
  }

  .mobile-scroll-hover {
    -webkit-transform: scale(1.2);
    -moz-transform: scale(1.2);
    -o-transform: scale(1.2);
    transform: scale(1.2);
  }

  .body-text-desc {
    font-size: 14px !important;
  }
  .gradient-text-features {
    font-size: 3rem !important;
  }

  .gradient-text {
    line-height: 3rem;
    font-size: 2.5rem !important;
  }

  .card-color-1 {
    -webkit-box-shadow: 0 0 20px#dda50a !important;
    -moz-box-shadow: 0 0 20px #dda50a !important;
    box-shadow: 0 0 20px #dda50a !important;
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 1;
    grid-row-end: 2;
  }

  .card-color-2 {
    -webkit-box-shadow: 0 0 20px #0addcb !important;
    -moz-box-shadow: 0 0 20px #0addcb !important;
    box-shadow: 0 0 20px #0addcb !important;
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 2;
    grid-row-end: 3;
  }
  .card-color-3 {
    -webkit-box-shadow: 0 0 20px #57dd0a !important;
    -moz-box-shadow: 0 0 20px #57dd0a !important;
    box-shadow: 0 0 20px #57dd0a !important;
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 3;
    grid-row-end: 4;
  }
  .card-color-4 {
    -webkit-box-shadow: 0 0 20px #9a0add !important;
    -moz-box-shadow: 0 0 20px #9a0add !important;
    box-shadow: 0 0 20px #9a0add !important;
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 4;
    grid-row-end: 5;
  }
}
</style>
