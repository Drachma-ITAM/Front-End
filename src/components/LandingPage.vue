<template>
  <div class="landing-page">
    <hero-banner/>
  </div>
</template>

<script>
import Hero from './Hero'

export default {
  name: 'LandingPage',
  components: {
    'hero-banner': Hero
  }
}
</script>

<style scoped>
.landing-page {
  width: 100%;
}
</style>
