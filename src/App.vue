<template>
  <div id="app">
    <Header />
    <cards-list />
  </div>
</template>

<script>

import Header from './components/Global/Header/Header'
import CardsList from './components/Global/Cards/CardsList'

export default {
  name: 'App',
  components: { CardsList, Header }
}
</script>

<style lang="scss">
  @import 'assets/scss/main.scss';
</style>
