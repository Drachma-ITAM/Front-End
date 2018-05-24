<template>
  <div class="landing-page">
    <nav-bar/>
    <hero-banner/>
  </div>
</template>

<script>
import NavBar from './global/NavBar'
import Hero from './Hero'

export default {
  name: 'LandingPage',
  components: {
    'hero-banner': Hero,
    'nav-bar': NavBar
  }
}
</script>

<style scoped>
.landing-page {
  width: 100%;
}
</style>
