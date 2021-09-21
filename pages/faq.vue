<template>
  <div style="height: 100%; overflow-y: scoll">
    <div class="mask" style="width: 100vw; height: 100vh"></div>
    <FAQHeader />
    <FAQBody id="faq-body" style="margin-top: 4vh" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'The Merged Mined Network of Blockchains | FAQs',
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'FAQs',
          name: 'FAQs',
          content:
            'Quai is a scalable network of blockchains designed for the future. Visit our site to learn more!',
        },
      ],
    }
  },
}
</script>

<style scoped>
.mask {
  height: 100%;
  background: transparent;
  background-image: url('./static/wolfram/wave.svg');
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
}
</style>
