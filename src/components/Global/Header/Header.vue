<template>
  <div class="header-wrap b-wrap">
    <header class="header">
      <div class="mobile-ui">
        <a href="/" class="logo">
          <img src="../../../assets/svg/logo.svg" alt="" class="logo-icon">
          <span class="logo-text">Midas</span>
        </a>
        <span
          @click="mobMenu = !mobMenu"
          :class="['menu-toggle',{'active': mobMenu}]"
        >
          menu
        </span>
      </div>
      <div :class="['menu-global',{'show-it': mobMenu}]">
        <div class="menu-logo-group">
          <a href="/" class="logo">
            <img src="../../../assets/svg/logo.svg" alt="" class="logo-icon">
            <span class="logo-text">Midas<span class="additional">.Investments</span></span>
          </a>
          <header-menu-list :items="platformMenu" />
        </div>
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
            <div class="account-data">
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
              </nav>
            </div>
          </li>
        </ul>
      </div>
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
      mobMenu: false,
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
          name: 'Profile'
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
