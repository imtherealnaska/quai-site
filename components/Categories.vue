<template>
  <div style="height: 100%">
    <v-container>
      <v-lazy>
        <v-row justify="space-between" style="margin-top: 10%; width: 100%">
          <v-col cols="4" sm="6" md="6" style="padding-right: 30px">
            <div class="quai-category-card-1" style="width: 100%">
              <img
                class="center-wolfram wolfram-bg"
                alt="Wolfram Mesh"
                src="wolfram/mesh.svg"
                style="height: 900px"
              />
              <v-card-text>
                <p
                  class="text-h3 gradient-text-1"
                  style="font-size: 5 rem !important"
                >
                  Payments
                </p>
                <div class="text--primary">
                  A description of what can be done<br />
                  with Quai
                </div>
              </v-card-text>
              <v-card-actions>
                <v-btn text color="#dda50a"> Learn More </v-btn>
              </v-card-actions>
            </div>
            <div
              elevation="2"
              class="quai-category-card-3"
              style="width: 100%; margin-top: 20%"
            >
              <img
                class="center-wolfram wolfram-bg"
                alt="Wolfram Web"
                src="wolfram/web.svg"
                style="height: 700px"
              />
              <v-card-text>
                <p class="text-h3 gradient-text-3">NFTs</p>
                <div class="text--primary">
                  A description of what can be done<br />
                  with Quai
                </div>
              </v-card-text>
              <v-card-actions>
                <v-btn text color="#0addcb"> Learn More </v-btn>
              </v-card-actions>
            </div>
          </v-col>
          <v-col cols="2" sm="6" md="6" style="padding-left: 30px">
            <v-card
              elevation="2"
              class="quai-category-card-2"
              style="width: 100%; margin-top: 20%"
            >
              <img
                class="center-wolfram wolfram-bg"
                alt="Wolfram Leaves"
                src="wolfram/leaves.svg"
                style="height: 600px"
              />
              <v-card-text>
                <p class="text-h3 gradient-text-2">DeFi</p>
                <div class="text--primary">
                  A description of what can be done<br />
                  with Quai
                </div>
              </v-card-text>
              <v-card-actions>
                <v-btn text color="#57dd0a"> Learn More </v-btn>
              </v-card-actions>
            </v-card>
            <v-card
              elevation="2"
              class="quai-category-card-4"
              style="width: 100%; margin-top: 20%"
            >
              <img
                class="center-wolfram wolfram-bg"
                alt="Wolfram Pillow"
                src="wolfram/pillow.svg"
                style="height: 500px"
              />
              <v-card-text>
                <p class="text-h3 gradient-text-4">Gaming</p>
                <div class="text--primary">
                  Quai offers a low cost environment for
                  <a
                    href="https://github.com/spruce-solutions/go-quai/pull/78"
                    target="_blank"
                    >blockchain based gaming</a
                  >
                </div>
              </v-card-text>
              <v-card-actions>
                <v-btn text color="#9a0add"> Learn More </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-lazy>
    </v-container>
  </div>
</template>

<style scoped>
.quai-category-card-1 {
  -webkit-box-shadow: 0 0 20px#dda50a !important;
  -moz-box-shadow: 0 0 20px #dda50a !important;
  box-shadow: 0 0 20px #dda50a !important;
  background-color: none !important;
  height: 600px;
  overflow: hidden;
  border-radius: 25px;
  position: relative;
}

.quai-category-card-2 {
  -webkit-box-shadow: 0 0 20px #57dd0a !important;
  -moz-box-shadow: 0 0 20px #57dd0a !important;
  box-shadow: 0 0 20px #57dd0a !important;
  background-color: none !important;
  height: 600px;
  overflow: hidden;
  border-radius: 25px;
  position: relative;
}

.quai-category-card-3 {
  -webkit-box-shadow: 0 0 20px #0addcb !important;
  -moz-box-shadow: 0 0 20px #0addcb !important;
  box-shadow: 0 0 20px #0addcb !important;
  background-color: none !important;
  height: 600px;
  overflow: hidden;
  border-radius: 25px;
  position: relative;
}

.quai-category-card-4 {
  -webkit-box-shadow: 0 0 20px #9a0add !important;
  -moz-box-shadow: 0 0 20px #9a0add !important;
  box-shadow: 0 0 20px #9a0add !important;
  background-color: none !important;
  height: 600px;
  overflow: hidden;
  border-radius: 25px;
  position: relative;
}

.center-wolfram {
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.wolfram-bg {
  position: absolute;
  /* background by SVGBackgrounds.com */
  top: 0;
  -webkit-mask-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0),
    rgba(0, 0, 0, 1)
  );
  pointer-events: none;
}

.wolfram-bg:hover {
  transform: scale(
    1.05
  ); /* (150% zoom - Note: if the zoom is too large, it will go outside of the viewport) */
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
  background: linear-gradient(179deg, #9a0add, rgb(236, 55, 55));
  line-height: 5.5rem;
  font-size: 5rem !important;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
