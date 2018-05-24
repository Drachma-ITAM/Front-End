<template>
  <div class="landing-page">
    <nav-bar/>
    <hero-banner/>
    <info-bar/>
    <news-letter/>
  </div>
</template>

<script>
import NavBar from './global/NavBar'
import Hero from './Hero'
import Info from './Info'
import NewsLetter from './NewsLetter'

export default {
  name: 'LandingPage',
  components: {
    'hero-banner': Hero,
    'nav-bar': NavBar,
    'info-bar': Info,
    'news-letter': NewsLetter
  }
}
</script>

<style scoped>
.landing-page {
  width: 100%;
}
</style>
