<template>
  <div style="height: 100%; overflow-y: scoll">
    <HomeLanding />
    <HomeCategories style="margin-top: 20vh" />
    <!-- <HomeAbout style="margin-top: 20vh" /> -->
    <HomeRoadmap style="margin-top: 20vh; margin-bottom: 20vh" />
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

<style scoped></style>
