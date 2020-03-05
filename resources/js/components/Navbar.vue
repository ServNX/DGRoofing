<template>
  <header class="header">
    <b-navbar toggleable="lg" type="dark" variant="dark" sticky>
      <b-navbar-toggle target="nav-collapse" />

      <b-collapse id="nav-collapse" is-nav class="justify-content-center">
        <b-navbar-nav>
          <b-nav-item href="#">
            Home
          </b-nav-item>
          <b-nav-item-dropdown text="Services">
            <b-dropdown-item href="#">
              Roofing
            </b-dropdown-item>
            <b-dropdown-item href="#">
              Windows
            </b-dropdown-item>
            <b-dropdown-item href="#">
              Gutters
            </b-dropdown-item>
            <b-dropdown-item href="#">
              Siding
            </b-dropdown-item>
            <b-dropdown-item href="#">
              Doors
            </b-dropdown-item>
            <b-dropdown-item href="#">
              Commercial
            </b-dropdown-item>
          </b-nav-item-dropdown>
          <b-nav-item href="#">
            Our Work
          </b-nav-item>
          <b-nav-item href="#">
            Community
          </b-nav-item>
          <b-nav-item href="#">
            About
          </b-nav-item>
          <b-nav-item href="#">
            Contact
          </b-nav-item>
        </b-navbar-nav>

        <b-navbar-nav>
          <b-nav-item-dropdown no-caret>
            <template v-slot:button-content>
              <fa icon="user" fixed-width />
            </template>
            <b-dropdown-item href="#">
              <fa icon="cog" fixed-width />
              Profile
            </b-dropdown-item>
            <b-dropdown-item href="#">
              <fa icon="sign-out-alt" fixed-width />
              Sign Out
            </b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </header>
</template>

<style lang="scss" scoped>
  @import "../../sass/_variables.scss";

  header.header {
    position: relative;
    z-index: 15;

    .navbar {
      .navbar-nav {
        .nav-item {
          margin-right: 50px;
        }
      }
    }
  }
</style>

<script>
import {
  BNavbar,
  BNavbarNav,
  BNavbarToggle,
  BCollapse,
  BNavItem,
  BDropdownItem,
  BNavItemDropdown
} from 'bootstrap-vue'

// import LocaleDropdown from './LocaleDropdown'
// import AuthUserDropdown from './AuthUserDropdown'

export default {
  components: {
    BNavbar,
    BNavbarNav,
    BNavbarToggle,
    BCollapse,
    BNavItem,
    BDropdownItem,
    BNavItemDropdown
  },

  data () {
    return {
      appName: window.config.appName
    }
  },

  computed: {
    user () {
      return this.$store.getters['auth/user']
    }
  }
}
</script>
