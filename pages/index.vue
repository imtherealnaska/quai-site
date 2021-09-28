<template>
  <div style="height: 100%; overflow-y: scoll">
    <div class="mask" style="width: 100vw; height: 100vh"></div>
    <HomeLanding id="home" style="margin-top: 4vh" />
    <HomeCategories id="features" class="index-spacing-1" />
    <HomeAbout id="about" class="index-spacing-2" />
    <HomeRoadmap id="roadmap" class="index-spacing-2" />
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
        {
          name: 'dmca-site-verification',
          content: 'R2dCZFNJdkNQOUFMYndpZTlOYk0xdz090',
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

.index-spacing-1 {
  margin-top: 60vh;
}

.index-spacing-2 {
  margin-top: 15vh;
}

/* Portrait tablets and small desktops */
@media (max-width: 1880) {
  .index-spacing-1 {
    margin-top: 34vh;
  }

  .index-spacing-2 {
    margin-top: 20vh;
  }
}

/* Portrait tablets and small desktops */
@media (max-width: 768px) {
  .index-spacing-1 {
    margin-top: 12vh;
  }

  .index-spacing-2 {
    margin-top: 12vh;
  }
}
</style>
