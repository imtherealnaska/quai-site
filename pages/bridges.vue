<template>
  <div style="overflow: hidden; padding-bottom: 10%">
    <div class="merged-mining-bg"></div>
    <v-container id="card1" class="card-color-3">
      <v-card-text style="position: relative">
        <h3 class="text-h1 gradient-text gradient-text-3">
          Decentralized Bridges: Trustless Cross-Chain Value Transfers
        </h3>
        <div class="text--primary" style="pointer-events: none">
          Janus governs the transfer of value within and across the Quai
          Network.<br /><br />
        </div>
        <div class="body-text-desc">
          Summary

          The Quai Network utilizes coincident blocks created from merged mining
          to transfer state across blockchains. A coincident block is created when
          a block is mined which has sufficient difficulty to satisfy the mining 
          requirement in more than one blockchain that is being merged mined.  A
          coincident block creates a block header which is valid in more than
          one block chain, hence the name coincident block.  The valid header will
          have references to data in both of the blockchains, including the previous
          block hash, which then creates a hash link back to the previous coincident
          block and a provable reference to all of the state transitions that have occured
          between the current coincident block and the previous coincident block with
          the respective blockchain.  This allows a blockchain which periodically experience
          coincidence blocks to have provable references to adjacent blockchains which
          can be used to cause internal state transitions in the local blockchain.
          These internal transitions can be driven by a protocol level understanding
          of the adjacent blockchain state or it can be driven by smart contract level
          state transitions which are triggered by playing valid external state transition
          proofs to the local blockchain.  This creates a mechanism by which any merged mined
          blockchain can have decentralized atomic bridges between itself and the blockchains
          with which it is merged mined.

          Merged Mined Headers

          The heirarchy of blockchains in the Quai network are connected through merged mined
          blocks which are made possible through the creation of headers which have references
          to more than one blockchain.  The Quai blockchain header is structered as an array
          of 3 Ethereum like headers.  The set of headers contain a zone, region, and prime
          header which represents a slice of the hierarchy of blockchains in the Quai network.
          A location specification
          is added to the header which determines which zone blockchain the header pertains
          to, and the region and prime header's blockchains are then inferred as being
          the parent of the specified zone. Each element in the array references a state root which
          is valid for that header's corresponding blockchain if and only if the difficulty
          of the block that is found meets the required difficulty for it's respective blockchain.
          This means that very often only the zone header is valid and the region a prime header
          data is strictly surperfulous and creates no cononical record.  However, when the 
          difficulty of the found block becomes great enough to meet the region difficulty
          a valid region block is found and only the prime portion of the header is superfulous
          data.  This is a region coincident block because by definition, if the difficulty is met
          for a region block it will also be met for the zone which means the both a zone and region
          block are found simultaneously.



        </div>
      </v-card-text>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'The Merged Mined Network of Blockchains | Decentralized Bridges',
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'Decentralized Bridges',
          name: 'Decentralized Bridges',
          content:
            'Quai is a scalable network of blockchains designed for the future. Visit our site to learn more!',
        },
      ],
    }
  },
}
</script>

<style scoped>
.merged-mining-bg {
  width: 75vw;
  height: 98vh;
  background: transparent;
  background-image: url('./static/wolfram/leaves.png');
  background-size: cover;
  background-repeat: no-repeat;
  -webkit-mask-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0),
    60%,
    rgba(0, 0, 0, 1)
  );
  position: absolute;
  top: 0;
  right: 0;
}

.body-text-desc {
  font-size: 20px !important;
  pointer-events: none;
}

.card-color-3 {
  margin-top: 10%;
  border-radius: 20px;
}

.gradient-text {
  line-height: 5.5rem;
  font-size: 5rem !important;
  pointer-events: none;
}

.gradient-text-3 {
  background: linear-gradient(#57dd0a, rgb(55, 133, 236));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

@media (max-width: 900px) {
  .body-text-desc {
    font-size: 14px !important;
  }

  .gradient-text {
    line-height: 3rem;
    font-size: 3rem !important;
  }
}
</style>
