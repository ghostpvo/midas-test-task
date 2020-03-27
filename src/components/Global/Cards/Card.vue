<template>
  <li>
    <div class="title-wrap">
      <icon
        :icon="data.name"
        :tittle="`icon ${data.name}`"
      />
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
          {{ data.percent }}
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
          {{ data.percentDynamic }}
        </span>
        <icon
          :icon="data.isPositive ? 'arr-up' : 'arr-down'"
          :title="'progress arrow'"
        />
      </div>
    </div>
  </li>
</template>

<script>
import Icon from '../../Elements/Icon/Icon'
export default {
  name: 'Card',
  components: { Icon },
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
