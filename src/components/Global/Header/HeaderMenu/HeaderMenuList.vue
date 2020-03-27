<template>
  <nav class="header-menu">
    <Header-menu-item
      v-for="(item, index) in items"
      :key="`menu-item-${index}`"
      :to="item.to"
      :name="item.name"
    />
  </nav>
</template>

<script>
import HeaderMenuItem from './HeaderMenuItem'
export default {
  name: 'HeaderMenuList',
  components: { HeaderMenuItem },
  props: {
    items: {
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "header-menu";
</style>
