<template>
  <v-container>
    <v-expansion-panels>
      <v-expansion-panel v-for="(item, i) in list" :key="i">
        <v-expansion-panel-header> {{ item.q }} </v-expansion-panel-header>
        <v-expansion-panel-content style="padding-top: 10px">
          {{ item.a }}
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    list: [
      {
        q: 'What is Quai?',
        a: 'Quai is a merged mined network of blockchains. By duplication blockchains Quai Network dramatically increases throughput of transactions.',
      },
      {
        q: 'How does Quai work?',
        a: 'Quai Network works by interweaving hierarchical blockchain networks through merged mining.',
      },
      {
        q: 'What is Merged Mining?',
        a: 'Merged Mining is the process of sharing hashrate across different blockchains. A Quai block header contains data for a Prime, Region, and Zone blockchain. The validity is determined by the amount of work found for the header.',
      },
      {
        q: 'What is a coincident block?',
        a: 'A coincident block is a block that applies to more than one blockchain. A Prime block is a coincident block of a Region and Zone. A Region block is a coincident block for a Zone.',
      },
      {
        q: 'How does Quai use a coincident block?',
        a: 'Quai uses coincident blocks to trace state changes. Coincident blocks provide linkages that can be traced through Region or Prime. These linkages allow nodes to retrieve state modifications that happen outside of their own blockchain.',
      },
      {
        q: 'Why was Quai created?',
        a: 'Quai was created to provide scalable, secure, and decentralized value transfers.',
      },
      {
        q: 'What do I gain from using Quai?',
        a: 'As a user, Quai will provide an ecosystem of tradeoffs for decentralization and time. Prime being the most decentralized / congested and Zones being less decentralized / congested. ',
      },
      { q: 'Is Quai EVM compatible?', a: 'Yes!' },
      {
        q: 'What projects will be launching on Quai?',
        a: 'Stay tuned to find out!',
      },
    ],
  }),
  methods: {
    openLink(link) {
      window.open(link, '_blank')
    },
  },
}
</script>

<style scoped>
>>> .v-expansion-panel-header {
  background-color: #121212 !important;
}

.theme--dark.v-expansion-panels .v-expansion-panel {
  background-color: rgb(236, 77, 55, 0.7) !important;
}

.v-expansion-panel-content__wrap {
}
</style>
