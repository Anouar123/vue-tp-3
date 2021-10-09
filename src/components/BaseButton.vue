<template>
  <div id="buttons">
    <button 
    id="base-button"
    class="button"
    :style="cssVars"
    >
      BaseButton
    </button>
    <button 
    id="base-button-disabled"
    disabled
    class="button"
    :style="cssVars"
    >
      BaseButton Disabled
    </button>

    <button 
    id="base-button-time"
    class="button"
    :style="cssVars"
    >
      BaseButton Time
    </button>
  </div>
</template>


<script>


export default {
  name: 'BaseButton',
  components: {
  },
  props: {
    btnColor: Object
  },
  computed: {
    cssVars() {
      return {
        '--bg-color-primary': this.btnColor.primary.bg,
        '--bg-hover-color-primary': this.btnColor.primary.hoverBg,
        '--bg-focus-color-primary': this.btnColor.primary.focusBorder,
      }
    }
  }
}

</script>



<style scoped>
#buttons {
  width: 20rem;
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin: 0 auto;
}
.button {
  border: 1px solid transparent;
  border-radius: 15px;
  text-align: center;
  cursor: pointer;
  color: #fff;
  margin-top: 60px;
  height: 3rem;
  width: 6rem;
}
#base-button-disabled {
  background-color: #dcedc8;
}
#base-button {
  background-color: var(--bg-color-primary);
}
#base-button:hover {
  background-color: var(--bg-hover-color-primary);
}
.button:focus {
  border: var(--bg-focus-color-primary);
}
</style>
