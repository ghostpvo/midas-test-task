<template>
  <button :class="['button-main',{'big-mode': isBig}]">
    {{ title }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    title: {
      type: String,
      default: 'Button'
    },
    isBig: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "button";
</style>
