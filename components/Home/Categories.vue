<template>
  <div class="quai-cards-wrapper">
    <div class="quai-cards">
      <div class="quai-category-card features" style="width: 100%">
        <v-card-text>
          <p
            class="text-h3 gradient-text-features"
            style="font-size: 5 rem !important"
          >
            Features that drive Quai into the future.
          </p>
          <div class="text--primary"></div>
        </v-card-text>
      </div>
      <div class="quai-category-card card-color-1" style="width: 100%">
        <div class="floating-wolfram wolfram-bg-1"></div>
        <v-card-text>
          <p
            class="text-h3 gradient-text-1"
            style="font-size: 5 rem !important"
          >
            Hermes
          </p>
          <div class="text--primary">
            Hermes (/ˈhɜːrmiːz/; Greek: Ἑρμῆς) is an Olympian deity in ancient
            Greek religion and mythology. Hermes is considered the herald of the
            gods.<br />
            with Quai
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="#dda50a" style="cursor: pointer">
            Learn More
          </v-btn>
        </v-card-actions>
      </div>
      <div style="height: 300px"></div>
      <div class="quai-category-card card-color-3">
        <div class="floating-wolfram wolfram-bg-3"></div>
        <v-card-text>
          <p class="text-h3 gradient-text-2">Janus</p>
          <div class="text--primary">
            Janus (/ˈdʒeɪnəs/ JAY-nəs; Latin: Iānus) is the god of beginnings,
            gates, transitions, time, duality, doorways,[1] passages, frames,
            and endings.
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="#57dd0a"> Learn More </v-btn>
        </v-card-actions>
      </div>
      <div class="quai-category-card card-color-2">
        <div class="floating-wolfram wolfram-bg-2"></div>
        <v-card-text>
          <p class="text-h3 gradient-text-3">Plutus</p>
          <div class="text--primary">
            Plutus (/ˈpluːtəs/; Greek: Πλοῦτος, translit. Ploûtos, lit.
            "wealth") is the Greek god of wealth.
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="#0addcb"> Learn More </v-btn>
        </v-card-actions>
      </div>
      <div class="quai-category-card card-color-4">
        <div class="floating-wolfram wolfram-bg-4"></div>
        <v-card-text>
          <p class="text-h3 gradient-text-4">Ares</p>
          <div class="text--primary">
            Ares (/ˈɛəriːz/; Ancient Greek: Ἄρης) is the Greek god of courage
            and war.<br />
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="#9a0add"> Learn More </v-btn>
        </v-card-actions>
      </div>
    </div>
  </div>
</template>

<style scoped>
.quai-cards-wrapper {
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  -webkit-box-pack: center;
  justify-content: center;
  margin-bottom: 7em;
  padding: 0px 2em;
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

.gradient-text-features {
  background: linear-gradient(150deg, white, silver);
  line-height: 5.5rem;
  font-size: 4rem !important;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
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

.floating-wolfram:hover {
  -webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
  rotation: 0.01; /* add to force matrix3d() */
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

.gradient-text-1 {
  background: linear-gradient(150deg, #dda50a, #ec4d37ff);
  line-height: 5.5rem;
  font-size: 5rem !important;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradient-text-2 {
  background: linear-gradient(#57dd0a, rgb(55, 133, 236));
  line-height: 5.5rem;
  font-size: 5rem !important;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradient-text-3 {
  background: linear-gradient(179deg, #0addcb, rgb(103, 55, 236));
  line-height: 5.5rem;
  font-size: 5rem !important;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradient-text-4 {
  background: linear-gradient(160deg, #9a0add, rgb(236, 55, 55));
  line-height: 5.5rem;
  font-size: 5rem !important;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

@media (max-width: 700px) {
  .quai-cards {
    display: grid;
    grid-template-columns: repeat(1, minmax(0px, 616px));
    grid-template-rows: repeat(10, minmax(0px, 300px));
    grid-auto-rows: 1fr;
    gap: 2.5em;
  }

  .features {
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 1;
    grid-row-end: 2;
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
}
</style>
