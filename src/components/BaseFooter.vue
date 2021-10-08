<template>
<slot name="bottom"></slot>
</template>

<script>

export default {
  name: 'BaseFooter',
  components: {
  }
}
</script>

<style>
#base-footer {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  position: fixed;
  bottom: 1rem;
}
</style>
