<template>
    <slot name="top"></slot>
</template>
<script>

export default {
  name: 'BaseHeader',
  components: {
  }
}
</script>

<style>
#base-header {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
