<template>
  <div id="buttons">
    <button id="base-button">
      BaseButton
    </button>
    <button 
    id="base-button-disabled"
    disabled
    >
      BaseButton Disabled
    </button>
  </div>
</template>

<script>
export default {
  name: 'BaseButton',
  components: {
  }
}
</script>

<style>
#buttons {
  width: 20rem;
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin: 0 auto;
}
#base-button, #base-button-disabled {
  border: 1px solid transparent;
  border-radius: 15px;
  text-align: center;
  color: #fff;
  margin-top: 60px;
  height: 3rem;
  width: 6rem;
}
#base-button {
  background-color: #00c853;
}
#base-button:hover {
  background-color: #2e7d32;
}
#base-button-disabled {
  background-color: #dcedc8;
}
</style>
