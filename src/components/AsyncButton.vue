<template>
<base-button
    :disabled="isPending"
    :btn-color="colorPalette"
    @click.stop.prevent="createDebounce"
  >
    <font-awesome-icon 
      v-if="isPending"
      :icon="['fas', 'circle-notch']"
      pulse
    />

    <slot />
  </base-button>
</template>

<script>
import BaseButton from './BaseButton.vue'
const colorPalette = {
  primary: { bg: '#42b983', hoverBg: '#4cce93', focusBorder: '#47d696' },
  warn: { bg: '#ff5722', hoverBg: '#ff7043', focusBorder: '#ff8a65' },
  danger: { bg: '#e53935', hoverBg: '#ef5350', focusBorder: '#e57373' },
}
export default {
  name: 'AsyncButton',
  components: { 
      'base-button': BaseButton 
      },
  inheritAttrs: false,
  data: () => ({
      colorPalette,
      isPending: false
  }),

  methods: {
    handleClick () {
        console.log('function called')
      this.isPending = true
    },
    createDebounce () {
        if(this.isPending){
            setTimeout(() => {
                this.handleClick();
            }, 2000)
        } else this.handleClick();
    },
  }
}
</script>