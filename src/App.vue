<template>
  <base-layout/>
  <home-page />
</template>

<script>
import BaseLayout from './layout/BaseLayout.vue';
import HomePage from './pages/HomePage.vue'
export default {
  name: 'App',
  components: {
    'base-layout': BaseLayout,
    'home-page': HomePage
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
