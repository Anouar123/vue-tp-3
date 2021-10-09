<template>
    <div id="home-page">Welcome to the home page!</div>
    <async-button />
</template>

<script>
import AsyncButton from '../components/AsyncButton.vue';
export default {
  name: 'HomePage',
  components: {
    'async-button': AsyncButton,
  },
  props: {
    color: {
      type: String,
      default: 'primary'
    }
  },
}
</script>

<style>
#home-page {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
