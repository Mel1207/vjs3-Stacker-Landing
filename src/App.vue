<template>
  <Navigation />

  <button @click="redirect">Redirect</button>
  <button @click="back">Go Back</button>
  <button @click="forward">Go Forward</button>

  <router-view/>
  <Footer />
</template>

<script>
import Navigation from './components/Navigation/Navigation.vue'
import Footer from './components/Footer/Footer.vue'

export default {
  components: { Navigation, Footer },
  methods: {
    redirect() {
      this.$router.push({ name: 'Home'})
    },
    back() {
      this.$router.go(-1)
    },
    forward() {
      this.$router.go(1)
    }
  }
}
</script>