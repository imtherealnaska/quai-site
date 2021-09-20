<template>
  <div style="height: 100%">
    <v-container>
      <v-timeline>
        <v-timeline-item
          v-for="(item, i) in items"
          :key="i"
          :color="item.color"
          small
          class="quai-timeline-item"
        >
          <template v-slot:opposite>
            <span
              :class="`headline font-weight-bold ${item.color}--text`"
              v-text="item.date"
            ></span>
          </template>
          <div
            class="roadmap-card"
            :class="
              (item.right ? 'text-right' : '',
              item.completed ? 'timeline-completed' : 'timeline-uncompleted')
            "
          >
            <v-card-text>
              <p class="text-h3 gradient-text-1">
                {{ item.title }}
              </p>
              <div style="overflow-wrap: break-word; word-wrap: break-word">
                {{ item.description }}
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
        date: 'Q4 2018',
        title: 'BlockReduce Publication',
        description: 'Initial BlockReduce paper and mechanism design',
        completed: true,
      },
      {
        color: '#e6614eff',
        date: 'Q3 2019',
        title: 'NSF Funding',
        description: 'Initial backing from National Science Foundation (NSF)',
        right: true,
        completed: true,
      },
      {
        color: '#e6614eff',
        date: 'Q1 2021',
        title: 'Seed Funding',
        description: '',
        completed: true,
      },
      {
        color: 'white',
        date: 'Q4 2021',
        title: 'Quai Testnet Launch',
        description: 'Security Hardeneing\nFinal Validations',
        right: true,
      },
      {
        color: 'white',
        date: 'Q1 2022',
        title: 'Tool Ramp-Up',
        description: 'Block Explorer\nNetwork Analyzer',
      },
      {
        color: 'white',
        date: 'Q2 2022',
        title: 'Quai Mainnet Launch',
        description:
          'Full launch with bootstrapped mining\nMerged mining on top of Bitcoin and Ethereum',
        right: true,
      },
      {
        color: 'white',
        date: 'Beyond',
        title: 'Incentivization Programs',
        description:
          'Liquidity mining programs\nEthereum state snapshot airdrops\nNFT drops',
      },
    ],
  }),
}
</script>
<style scoped>
.timeline-completed {
  -webkit-box-shadow: 0 0 20px #ec4d37ff;
  -moz-box-shadow: 0 0 20px #ec4d37ff;
  box-shadow: 0 0 20px #ec4d37ff;
}

.timeline-uncompleted {
  -webkit-box-shadow: 0 0 20px white;
  -moz-box-shadow: 0 0 20px white;
  box-shadow: 0 0 20px white;
}

.roadmap-card {
  overflow: hidden;
  border-radius: 25px;
  width: max-content !important;
}

.gradient-text-1 {
  background: linear-gradient(120deg, #ec4d37ff, #ffa500);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-size: 5rem;
}

.v-timeline-item_body {
  width: 50px !important;
}

.v-timeline::before {
  top: 55px;
  height: calc(100% - 110px);
}

@media (max-width: 900px) {
  .roadmap-card {
    overflow: hidden;
    border-radius: 25px;
    width: 100% !important;
    font-size: 30px;
    max-width: 100% !important;
    margin-top: 30px;
  }

  .v-timeline-item__body {
    max-width: 400px !important;
  }

  .gradient-text-1 {
    background: linear-gradient(120deg, #ec4d37ff, #ffa500);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-size: 25px !important;
  }

  .v-timeline-item {
    width: 100% !important;
    display: flex !important;
    align-items: center !important;
    justify-content: center !important;
  }

  .v-timeline:not(.v-timeline--dense):not(.v-timeline--reverse)
    .v-timeline-item:nth-child(odd):not(.v-timeline-item--before),
  .v-timeline:not(.v-timeline--dense):not(.v-timeline--reverse)
    .v-timeline-item--after {
    flex-direction: column-reverse !important;
  }

  .v-timeline:not(.v-timeline--dense):not(.v-timeline--reverse)
    .v-timeline-item:nth-child(even):not(.v-timeline-item--before),
  .v-timeline:not(.v-timeline--dense):not(.v-timeline--reverse)
    .v-timeline-item--after {
    flex-direction: column-reverse !important;
  }

  >>> .v-timeline:not(.v-timeline--dense):not(.v-timeline--reverse)
    .v-timeline-item:nth-child(odd):not(.v-timeline-item--before)
    .v-timeline-item__body,
  .v-timeline:not(.v-timeline--dense):not(.v-timeline--reverse)
    .v-timeline-item--after
    .v-timeline-item__body {
    max-width: calc(100% - 48px) !important;
  }

  >>> .v-timeline:not(.v-timeline--dense):not(.v-timeline--reverse)
    .v-timeline-item:nth-child(even):not(.v-timeline-item--before)
    .v-timeline-item__body,
  .v-timeline:not(.v-timeline--dense):not(.v-timeline--reverse)
    .v-timeline-item--after
    .v-timeline-item__body {
    max-width: calc(100% - 48px) !important;
  }

  >>> .v-timeline-item__body {
    width: 100% !important;
  }

  >>> .v-timeline::before {
    height: 0;
  }
}
</style>
