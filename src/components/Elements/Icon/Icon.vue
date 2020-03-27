<template>
  <svg
    :class="iconId"
    class="icon"
    viewBox="0 0 100 100"
  >
    <use :xlink:href="getSprite(iconId)">
      {{ tittle }}
    </use>
  </svg>
</template>

<script>
export default {
  name: 'Icon',
  props: {
    icon: {
      type: String,
      default: ''
    },
    tittle: {
      type: String,
      default: ''
    },
    isActive: {
      type: Boolean,
      default: false
    }
  },
  computed: {
    iconId () {
      if (this.isActive) {
        return this.icon + '-active'
      } else {
        return this.icon
      }
    }
  },
  methods: {
    getSprite (type) {
      return `/static/sprite/sprite.svg#${type}`
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "icon";
</style>
