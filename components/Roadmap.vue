<template>
  <div style="height: 100%">
    <v-container>
      <v-timeline>
        <v-timeline-item
          v-for="(item, i) in items"
          :key="i"
          :color="item.color"
          small
        >
          <template v-slot:opposite>
            <span
              :class="`headline font-weight-bold ${item.color}--text`"
              v-text="item.date"
            ></span>
          </template>
          <div
            class="roadmap-card"
            style="width: 100%"
            :class="item.right ? 'text-right' : ''"
          >
            <v-card-text>
              <p
                class="text-h3 gradient-text-1"
                style="font-size: 5 rem !important"
              >
                {{ item.title }}
              </p>
              <div class="text--primary">
                <pre
                  style="font-family: Roboto, sans-serif; line-height: 1.5"
                  >{{ item.description }}</pre
                >
              </div>
            </v-card-text>
          </div>
        </v-timeline-item>
      </v-timeline>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        color: '#e6614eff',
        date: 'Q3 2021',
        title: 'Testnet Launch',
        description: 'Security Hardeneing\nFinal Validations',
      },
      {
        color: '#e6614eff',
        date: 'Q4 2021',
        title: 'Tool Ramp-Up',
        description: 'Block Explorer\nNetwork Analyzer',
        right: true,
      },
      {
        color: '#e6614eff',
        date: 'Q1 2022',
        title: 'Mainnet Launch',
        description:
          'Full launch with bootstrapped mining\nMerged mining on top of Bitcoin and Ethereum',
      },
      {
        color: '#e6614eff',
        date: 'Beyond',
        title: 'Incentivization Programs',
        description:
          'Liquidity mining programs\nEthereum state snapshot airdrops\nNFT drops',
        right: true,
      },
    ],
  }),
}
</script>
<style scoped>
.roadmap-card {
  -webkit-box-shadow: 0 0 20px red;
  -moz-box-shadow: 0 0 20px red;
  box-shadow: 0 0 20px red;
  overflow: hidden;
  border-radius: 25px;
}
</style>
