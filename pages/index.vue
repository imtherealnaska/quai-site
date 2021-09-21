<template>
  <div style="height: 100%; overflow-y: scoll">
    <div class="mask" style="width: 100vw; height: 100vh"></div>
    <HomeLanding id="home" style="margin-top: 4vh" />
    <HomeCategories id="features" style="margin-top: 34vh" />
    <HomeAbout id="about" style="margin-top: 20vh" />
    <HomeRoadmap id="roadmap" style="margin-top: 20vh; margin-bottom: 20vh" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Merged Mined Blockchain Solution',
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
</style>
