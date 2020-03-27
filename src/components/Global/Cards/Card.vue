<template>
  <li class="card-item">
    <div class="title-wrap">
      <div class="card-icon-wrap">
        <img
          class="card-icon"
          :src="require(`../../../assets/svg/icons/${data.name}.svg`)"
          :alt="data.name"
        />
      </div>
      <div class="name-wrap">
        <strong class="name-main">
          {{ data.name }}
        </strong>
        <span class="name-sub">
          {{ data.name }}
        </span>
      </div>
      <div class="percent-wrap">
        <span class="percent-title">
          ROI
        </span>
        <span class="percent-amount">
          {{ data.percent }}%
        </span>
      </div>
    </div>
    <div class="card-amount">
      <span class="amount-currency">
        {{ data.amountCurrency }}
      </span>
      <span class="amount-data">
        {{ data.amount }}
      </span>
    </div>
    <div class="number-info">
      <span class="number-data">
        {{ data.course }}
      </span>
      <span class="number-context">
        {{ data.name }}
      </span>
    </div>
    <div class="day-stat">
      <div class="number-info">
        <span class="number-data">
          {{ data.spentByDay }}
        </span>
          <span class="number-context">
          {{ data.amountCurrency }}/DAY
        </span>
      </div>
      <div
        :class="['percent-dynamic', {'is-negative': !data.isPositive}]"
      >
        <span>
          {{ data.isPositive ? '+' : '-' }}
        </span>
        <span>
          {{ data.percentDynamic }}%
        </span>
        <img
          class="progress-arrow"
          alt="progress arrow"
          :src="require(`../../../assets/svg/icons/${data.isPositive ? 'arr-up' : 'arr-down'}.svg`)"
        />
      </div>
    </div>
  </li>
</template>

<script>
export default {
  name: 'Card',
  props: {
    data: {
      type: Array
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "cards-list";
</style>
