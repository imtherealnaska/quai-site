<template>
  <div class="quai-cards-wrapper">
    <div class="quai-cards">
      <div class="quai-category-card card-color-1" style="width: 100%">
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
        <div class="floating-wolfram wolfram-bg-1"></div>
      </div>
      <div style="height: 300px"></div>
      <div class="quai-category-card card-color-3">
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
        <div class="floating-wolfram wolfram-bg-3"></div>
      </div>
      <div class="quai-category-card card-color-2">
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
        <div class="floating-wolfram wolfram-bg-2"></div>
      </div>
      <div class="quai-category-card card-color-4">
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
        <div class="floating-wolfram wolfram-bg-4"></div>
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
  gap: 2.5em;
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
}

.wolfram-bg-1 {
  background-image: url('./static/wolfram/mesh.svg');
}

.wolfram-bg-2 {
  background-image: url('./static/wolfram/web.svg');
}
.wolfram-bg-3 {
  background-image: url('./static/wolfram/leaves.svg');
}
.wolfram-bg-4 {
  background-image: url('./static/wolfram/pillow.svg');
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
