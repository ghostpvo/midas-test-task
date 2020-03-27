<template>
  <a :href="to" class="menu-item">{{name}}</a>
</template>

<script>
export default {
  name: 'HeaderMenuItem',
  props: {
    to: {
      type: String,
      default: '/'
    },
    name: {
      type: String,
      default: 'Unnamed link'
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "header-menu";
</style>
