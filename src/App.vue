<template>
  <Navigation />
  <router-view/>
</template>

<script>
import Navigation from './components/Navigation/Navigation.vue'

export default {
  components: { Navigation }
}
</script>