<template>
  <Navigation />
  <router-view/>
  <Footer />
</template>

<script>
import Navigation from './components/Navigation/Navigation.vue'
import Footer from './components/Footer/Footer.vue'

export default {
  components: { Navigation, Footer }
}
</script>