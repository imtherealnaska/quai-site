<template>
  <div style="height: 100%">
    <v-container>
      <v-lazy>
        <v-row justify="space-between" style="margin-top: 10%; width: 100%">
          <v-col cols="4" sm="6" md="6">
            <v-card
              elevation="2"
              class="quai-category-card"
              style="width: 100%"
            >
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
              </v-card-actions></v-card
            >
          </v-col>
          <v-col cols="2" sm="6" md="6">
            <div class="quai-category-card">
              <img
                class="center-wolfram"
                alt="Wolfram Mesh"
                src="wolfram/mesh.svg"
                style="height: 500px"
              />
            </div>
          </v-col>
        </v-row>
      </v-lazy>
      <v-lazy>
        <v-row justify="space-between" style="margin-top: 10%; width: 100%">
          <v-col cols="4" sm="6" md="6">
            <div class="quai-category-card">
              <img
                class="center-wolfram"
                alt="Wolfram Leaves"
                src="wolfram/leaves.svg"
                style="height: 600px"
              />
            </div>
          </v-col>
          <v-col cols="2" sm="6" md="6">
            <v-card
              elevation="2"
              class="quai-category-card"
              style="width: 100%"
            >
              <v-card-text>
                <p class="text-h3 gradient-text-2">DeFi</p>
                <div class="text--primary">
                  A description of what can be done<br />
                  with Quai
                </div>
              </v-card-text>
              <v-card-actions>
                <v-btn text color="#57dd0a"> Learn More </v-btn>
              </v-card-actions></v-card
            >
          </v-col>
        </v-row>
      </v-lazy>
      <v-lazy>
        <v-row justify="space-between" style="margin-top: 10%; width: 100%">
          <v-col cols="4" sm="6" md="6">
            <v-card
              elevation="2"
              class="quai-category-card"
              style="width: 100%"
            >
              <v-card-text>
                <p class="text-h3 gradient-text-3">NFTs</p>
                <div class="text--primary">
                  A description of what can be done<br />
                  with Quai
                </div>
              </v-card-text>
              <v-card-actions>
                <v-btn text color="rgb(103, 55, 236)"> Learn More </v-btn>
              </v-card-actions></v-card
            >
          </v-col>
          <v-col cols="2" sm="6" md="6">
            <div class="quai-category-card">
              <img
                class="center-wolfram"
                alt="Wolfram Web"
                src="wolfram/web.svg"
                style="height: 700px"
              />
            </div>
          </v-col>
        </v-row>
      </v-lazy>
      <v-lazy>
        <v-row justify="space-between" style="margin-top: 10%; width: 100%">
          <v-col cols="4" sm="6" md="6">
            <div class="quai-category-card">
              <img
                class="center-wolfram"
                alt="Wolfram Split"
                src="wolfram/split.svg"
                style="height: 500px"
              />
            </div>
          </v-col>
          <v-col cols="2" sm="6" md="6">
            <v-card
              elevation="2"
              class="quai-category-card"
              style="width: 100%"
            >
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
              </v-card-actions></v-card
            >
          </v-col>
        </v-row>
      </v-lazy>
    </v-container>
  </div>
</template>

<style scoped>
.quai-category-card {
  -webkit-box-shadow: 0 0 20px white;
  -moz-box-shadow: 0 0 20px white;
  box-shadow: 0 0 20px white;
  height: 500px;
  overflow: hidden;
  border-radius: 25px;
}

.center-wolfram {
  display: block;
  margin-left: auto;
  margin-right: auto;
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
