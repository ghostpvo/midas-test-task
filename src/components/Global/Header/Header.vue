<template>
  <div class="header-wrap b-wrap">
    <header class="header">
      <header-menu-list :items="platformMenu"/>
      <a href="" class="logo">
        <img src="../../../assets/svg/logo.svg" alt="" class="logo-icon">
        <span class="logo-text">Midas.Investments</span>
      </a>
      <ul class="user-data">
        <li class="user-item purse-item">
          <span class="current-balance">
            {{ user.balance }}
          </span>
          <span class="current-currency">
            {{ user.currency }}
          </span>
        </li>
        <li class="user-item user-account">
          <span class="user-name">
            {{ user.name }}
          </span>
          <div v-if="false" class="account-data">
            <strong class="dropdown-title">
              {{ user.name }}
            </strong>
            <nav class="user-menu">
              <a
                v-for="(item, index) in userMenu"
                :key="`menu-item-${index}`"
                :href="item.to"
                class="user-menu-link">
                {{ item.name }}
              </a>
              <a href="" class="user-menu-link">Test link 2</a>
              <a href="" class="user-menu-link">Test link 3</a>
              <a href="" class="user-menu-link">Test link 4</a>
              <a href="" class="user-menu-link">Test link 5</a>
            </nav>
          </div>
        </li>
      </ul>
    </header>
  </div>
</template>

<script>
import HeaderMenuList from './HeaderMenu/HeaderMenuList'
export default {
  name: 'header',
  components: { HeaderMenuList },
  data () {
    return {
      platformMenu: [
        {
          to: '/',
          name: 'Platform'
        },
        {
          to: '/',
          name: 'Exchange'
        },
        {
          to: '/',
          name: 'Fline trading bot'
        },
        {
          to: '/',
          name: 'Burn-out'
        }
      ],
      userMenu: [
        {
          to: '/',
          name: 'Platform'
        },
        {
          to: '/',
          name: 'Profile'
        },
        {
          to: '/',
          name: 'BTC balance'
        },
        {
          to: '/',
          name: 'Fline trading  bot'
        },
        {
          to: '/',
          name: 'Midas coin'
        },
        {
          to: '/',
          name: 'Sign out'
        }
      ],
      user: {
        name: 'Lorem Ipsum Dolor Sit',
        balance: 0.165499466,
        currency: 'BTC'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "header";
</style>
