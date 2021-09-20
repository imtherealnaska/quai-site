<template>
  <v-footer dark padless style="height: 100%">
    <v-card flat tile class="footer-card lighten-1 white--text text-center">
      <v-card-text class="white--text pt-0">
        <v-row>
          <v-col v-for="(list, i) in lists" :key="i">
            <v-row v-for="item in list" :key="item.title">
              <v-btn color="white" text rounded class="my-2">
                <v-col class="footer-column"
                  >{{ item.title }}
                  <!-- <p style="font-size: 12px">{{ item.desc }}</p> -->
                </v-col>
              </v-btn>
            </v-row>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
    <v-row justify="center" no-gutters> </v-row>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    lists: [
      [
        { title: 'FAQs', desc: 'Got a burning question?' },
        { title: 'Wallet Setup', desc: 'Receive and use Quai' },
        { title: 'Developer Docs', desc: 'Start building on Quai' },
        { title: 'Block Explorer', desc: 'Coming soon' },
        { title: 'Network Analyzer', desc: 'Coming soon' },
      ],
      [
        { title: 'Mission', desc: 'Why was Quai built?' },
        { title: 'Careers', desc: 'Join our team' },
      ],
      [
        { title: 'Twitter', desc: 'Slide into our DMs' },
        { title: 'Discord', desc: 'Chat with our devs' },
        { title: 'Medium', desc: 'Read more about Quai' },
      ],
    ],
  }),
}
</script>

<style scoped>
.footer-card {
  width: 100%;
  height: 100%;
  padding-top: 30px;
  padding-bottom: 30px;
  padding-left: 15%;
  padding-right: 15%;
}

.footer-column {
  text-align: left !important;
  width: 10vw;
}

@media (max-width: 700px) {
  .footer-card {
    padding-left: 5%;
    padding-right: 5%;
  }

  .footer-column {
    font-size: 12px !important;
  }
}
</style>
