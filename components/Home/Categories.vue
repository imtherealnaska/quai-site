<template>
  <div class="quai-cards-wrapper">
    <div class="quai-cards">
      <div class="quai-category-card features" style="width: 100%">
        <v-card-text>
          <p class="text-h3 gradient-text-features">
            Features that drive Quai.
          </p>
          <div class="text--primary"></div>
        </v-card-text>
      </div>

      <div id="card1" class="quai-category-card card-color-1">
        <div
          class="floating-wolfram wolfram-bg-1"
          v-bind:class="[cardOneActive ? 'mobile-scroll-hover ' : '']"
        ></div>
        <v-card-text style="position: relative">
          <p class="text-h3 gradient-text gradient-text-1">Hermes</p>
          <div class="text--primary" style="pointer-events: none">
            Hermes (/ˈhɜːrmiːz/; Greek: Ἑρμῆς) is considered the herald of the
            gods.<br /><br />
          </div>
          <HelpersIntersectionObserver
            sentinal-name="card-1"
            @on-intersection-element="onIntersectionElement"
          >
          </HelpersIntersectionObserver>
          <div class="body-text-desc">
            Hermes governs the co-ordination of the all of the blockchains in
            the merged mined braid of Proof-of-Work (PoW) blockchains that make
            up the Quai network. She allows the network to handle more then 100
            times more transactions then traditional single-thread blockchains
            such as Bitcoin and Ethereum, while still allowing the chains to
            easily interact and perform transactions cross-chain intra-network
            in Layer 1. Hermes primarily employs the hierarchical longest chain
            rule as well as synchronous blocks to allow the deterministic and
            atomic propogation of cross-chain transitions.
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
        <div
          id="janusBg"
          class="floating-wolfram wolfram-bg-3"
          v-bind:class="[cardTwoActive ? 'mobile-scroll-hover ' : '']"
        ></div>
        <v-card-text style="position: relative">
          <p class="text-h3 gradient-text gradient-text-2">Janus</p>
          <div class="text--primary" style="pointer-events: none">
            Janus (/ˈdʒeɪnəs/ JAY-nəs; Latin: Iānus) is the god of beginnings,
            gates, transitions, time, duality, doorways,[1] passages, frames,
            and endings.<br /><br />
          </div>
          <HelpersIntersectionObserver
            sentinal-name="card-2"
            @on-intersection-element="onIntersectionElement"
          >
          </HelpersIntersectionObserver>
          <div class="body-text-desc">
            Janus governs the interfaces between the Quai Network and existing
            blockchains. He is able to incentivize merge mining of the Quai's
            PRIME blockchain by other networks which can then be used to make
            trustless bridgeless transactions possible. Janus controls which
            blockchains are trustlessly linked to the Quai Network.
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="#57dd0a" nuxt to="/bridges"> Learn More </v-btn>
        </v-card-actions>
      </div>
      <div id="card2" class="quai-category-card card-color-2">
        <div
          class="floating-wolfram wolfram-bg-2"
          v-bind:class="[cardThreeActive ? 'mobile-scroll-hover ' : '']"
        ></div>
        <v-card-text style="position: relative">
          <p class="text-h3 gradient-text gradient-text-3">Plutus</p>
          <div class="text--primary" style="pointer-events: none">
            Plutus (/ˈpluːtəs/; Greek: Πλοῦτος, translit. Ploûtos, lit.
            "wealth") is the Greek god of wealth.<br /><br />
          </div>
          <HelpersIntersectionObserver
            sentinal-name="card-3"
            @on-intersection-element="onIntersectionElement"
          >
          </HelpersIntersectionObserver>
          <div class="body-text-desc">
            Plutus governs the monetary policy of the Quai Network. He manages
            the supply of Quai tokens to adequately incentive miners to dedicate
            sufficient computing resources to provide only the amount of
            security needed by the network. Plutus will initially create an
            inflationary token supply, but will ultimately make the Quai token
            supply as deflationary as possible. Additionally, Plutus uses
            bonding rewards to stabalize the market price of the Quai token
            making it less volatile and more useful for transactions.
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="#0addcb" nuxt to="/tokenomics"> Learn More </v-btn>
        </v-card-actions>
      </div>
      <div id="card4" class="quai-category-card card-color-4">
        <div
          class="floating-wolfram wolfram-bg-4"
          v-bind:class="[cardFourActive ? 'mobile-scroll-hover ' : '']"
        ></div>
        <v-card-text style="position: relative">
          <p class="text-h3 gradient-text gradient-text-4">Ares</p>
          <div class="text--primary" style="pointer-events: none">
            Ares (/ˈɛəriːz/; Ancient Greek: Ἄρης) is the Greek god of courage
            and war.<br /><br />
          </div>
          <HelpersIntersectionObserver
            sentinal-name="card-4"
            @on-intersection-element="onIntersectionElement"
          >
          </HelpersIntersectionObserver>
          <div class="body-text-desc">
            Ares governs the incentives for defecting from traditional networks
            and using the Quai Network. Ares has incentives for individuals,
            developers, companies, central banks, and nation states to adopt the
            Quai Network. Many of these incentives are structured with geometric
            payouts which provide greater rewards to the first adopters in each
            category. Additionally, Ares may from time-to-time deploy high value
            incentives which may disrupt the operation of competing blockchains.
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
  methods: {
    onIntersectionElement(data) {
      if (data.name == 'card-1') {
        this.cardOneActive = data.intersect
      }
      if (data.name == 'card-2') {
        this.cardTwoActive = data.intersect
      }
      if (data.name == 'card-3') {
        this.cardThreeActive = data.intersect
      }
      if (data.name == 'card-4') {
        this.cardFourActive = data.intersect
      }
    },
  },
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
}

.quai-cards {
  display: grid;
  grid-template-columns: repeat(2, minmax(0px, 616px));
  grid-template-rows: repeat(5, minmax(0px, 300px));
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
  height: 600px;
}

.features {
  grid-column-start: 2;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 3;
}

.body-text-desc {
  font-size: 20px !important;
  pointer-events: none;
}

.gradient-text-features {
  background: linear-gradient(150deg, white, silver);
  line-height: 5.5rem;
  font-size: 4.5rem !important;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
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

#card1:hover > .wolfram-bg-1 {
  -webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
}

#card2:hover > .wolfram-bg-2 {
  -webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
}

#card3:hover > .wolfram-bg-3 {
  -webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
}

#card4:hover > .wolfram-bg-4 {
  -webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
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
  grid-row-start: 2;
  grid-row-end: 4;
}
.card-color-4 {
  -webkit-box-shadow: 0 0 20px #9a0add !important;
  -moz-box-shadow: 0 0 20px #9a0add !important;
  box-shadow: 0 0 20px #9a0add !important;
  grid-column-start: 2;
  grid-column-end: 2;
  grid-row-start: 4;
  grid-row-end: 6;
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
  line-height: 5.5rem;
  font-size: 5rem !important;
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
    grid-template-rows: repeat(9, minmax(0px, 275px));
    grid-auto-rows: 1fr;
    gap: 2.5em;
  }

  .quai-category-card {
    height: 550px;
  }

  .mobile-scroll-hover {
    -webkit-transform: scale(1.2);
    -moz-transform: scale(1.2);
    -o-transform: scale(1.2);
    transform: scale(1.2);
  }

  .features {
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 1;
    grid-row-end: 2;
  }

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

  .card-color-1 {
    -webkit-box-shadow: 0 0 20px#dda50a !important;
    -moz-box-shadow: 0 0 20px #dda50a !important;
    box-shadow: 0 0 20px #dda50a !important;
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 2;
    grid-row-end: 4;
  }

  .card-color-2 {
    -webkit-box-shadow: 0 0 20px #0addcb !important;
    -moz-box-shadow: 0 0 20px #0addcb !important;
    box-shadow: 0 0 20px #0addcb !important;
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 4;
    grid-row-end: 6;
  }
  .card-color-3 {
    -webkit-box-shadow: 0 0 20px #57dd0a !important;
    -moz-box-shadow: 0 0 20px #57dd0a !important;
    box-shadow: 0 0 20px #57dd0a !important;
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 6;
    grid-row-end: 8;
  }
  .card-color-4 {
    -webkit-box-shadow: 0 0 20px #9a0add !important;
    -moz-box-shadow: 0 0 20px #9a0add !important;
    box-shadow: 0 0 20px #9a0add !important;
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 8;
    grid-row-end: 10;
  }

  /* Apply left spacing just to the Janus image */
  /* #janusBg {
    margin-right: 400px;
  } */
}
</style>
