<template>
  <v-container>
    <v-expansion-panels>
      <v-expansion-panel v-for="(item, i) in list" :key="i">
        <v-expansion-panel-header> {{ item.q }} </v-expansion-panel-header>
        <v-expansion-panel-content>
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
      { q: 'What is Quai?', a: '' },
      { q: 'How does Quai work?', a: '' },
      { q: 'What is Merged Mining?', a: '' },
      { q: 'What is a coincident block?', a: '' },
      { q: 'How does Quai use a coincident block?', a: '' },
      { q: 'Why was Quai created?', a: '' },
      { q: 'What do I gain from using Quai?', a: '' },
      { q: 'Is Quai EVM compatible?', a: 'Yes!' },
      { q: 'What projects will be launching on Quai?', a: '' },
    ],
  }),
  methods: {
    openLink(link) {
      window.open(link, '_blank')
    },
  },
}
</script>
