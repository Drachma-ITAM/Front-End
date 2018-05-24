<template>
  <div class="landing-page">
    <nav-bar/>
    <hero-banner/>
    <info-bar/>
  </div>
</template>

<script>
import NavBar from './global/NavBar'
import Hero from './Hero'
import Info from './Info'

export default {
  name: 'LandingPage',
  components: {
    'hero-banner': Hero,
    'nav-bar': NavBar,
    'info-bar': Info
  }
}
</script>

<style scoped>
.landing-page {
  width: 100%;
}
</style>
