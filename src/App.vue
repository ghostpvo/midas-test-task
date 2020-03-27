<template>
  <div id="app">
    <Header />
    <cards-list class="b-wrap" />
    <Buttons />
  </div>
</template>

<script>

import Header from './components/Global/Header/Header'
import CardsList from './components/Global/Cards/CardsList'
import Buttons from './components/UiKit/Buttons/Buttons'

export default {
  name: 'App',
  components: { Buttons, CardsList, Header }
}
</script>

<style lang="scss">
  @import 'assets/scss/main.scss';
</style>
