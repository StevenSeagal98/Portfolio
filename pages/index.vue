<template>
  <div class="container-fluid d-flex flex-column p-0 m-0">
    <Navbar />
    <NewHero />
    <Footer />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',

  components: {

  },

  data() {
    return {
      tab: 'hero'
    }
  },

  methods: {
    setTabTrue(selection) {
      this.tab = selection;
    },
  },

  mounted() {
    this.setTabTrue('hero')
  }
}
</script>

<style scoped>
.container-fluid {
  background: rgba(20, 20, 43, 1);
}

* {
  max-height: 100vh;
  overflow-y: hidden;
}
</style>