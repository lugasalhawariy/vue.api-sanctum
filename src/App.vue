<template>
  <div id="app">
    <Navigation/>
    <router-view/>
  </div>
</template>

<script>
import Navigation from '../src/components/Navigation.vue'

export default {
  components: {
    Navigation
  }
}
</script>

