<template>
  <div style="height: 100%; overflow-y: scoll">
    <div class="mask" style="width: 100vw; height: 100vh"></div>
    <HomeLanding id="home" style="margin-top: 4vh" />
    <HomeCategories id="features" class="index-spacing" />
    <HomeAbout id="about" class="index-spacing" />
    <HomeRoadmap id="roadmap" class="index-spacing" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'The Merged Mined Network of Blockchains',
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'Home',
          name: 'Home',
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

.index-spacing {
  margin-top: 34vh;
}

/* Portrait tablets and small desktops */
@media (min-width: 768px) and (max-width: 991px) {
  .index-spacing {
    margin-top: 15vh;
  }
}
</style>
