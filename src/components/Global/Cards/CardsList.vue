<template>
  <div class="cards-blc">
    <ul class="cards-list">
      <card
        v-for="(card, index) in cards"
        :key="`card-${index}`"
        :data="card"
      />
    </ul>
  </div>
</template>

<script>
import Card from './Card'
export default {
  name: 'CardsList',
  components: { Card },
  data () {
    return {
      cards: [
        {
          name: 'dash',
          percent: '75',
          amountCurrency: '$',
          amount: 1183.74,
          course: 17.55,
          spentByDay: 0.17,
          percentDynamic: 4.43,
          isPositive: true
        },
        {
          name: 'dash',
          percent: '75',
          amountCurrency: '$',
          amount: 1183.74,
          course: 17.55,
          spentByDay: 0.17,
          percentDynamic: 4.43,
          isPositive: false
        },
        {
          name: 'dash',
          percent: '75',
          amountCurrency: '$',
          amount: 1183.74,
          course: 17.55,
          spentByDay: 0.17,
          percentDynamic: 4.43,
          isPositive: true
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "cards-list";
</style>
