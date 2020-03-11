<template>
  <header class="header">
    <b-container fluid>
      <b-row>
        <b-col lg="2" class="d-none d-lg-block">
          <b-img class="logo" src="dist/img/logo.png" width="120" alt="D & G Roofing Logo" />
        </b-col>
        <b-col md="12" lg="6" align-self="center">
          <b-navbar toggleable="lg" type="light">
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
        </b-col>
        <b-col xl="4" class="d-none d-xl-block">
          <b-container class="d-flex justify-content-end" fluid>
            <div class="call-today">
              <div class="phone-number">
                <fa icon="phone" class="text-dark" />
                <a href="tel:1-937-439-0554">937-439-0554</a>
              </div>
              <span>Call today for a free estimate.</span>
            </div>
          </b-container>
        </b-col>
      </b-row>
    </b-container>
  </header>
</template>

<style lang="scss" scoped>
  @import "../../sass/_variables.scss";

  .header {
    position: relative;
    z-index: 15;
    border-bottom: 2px solid $red;
    padding: 10px 0 10px 0;

    .logo {
      margin-left: 20px;
    }

    .btn {
      display: block;
      border: 1px solid $red;
      border-radius: 4px;
      color: $red;
      font-weight: 700;
      font-size: 14px;
      padding: 10px 25px;
      margin: 45px 0 45px 0;
      transition: all 0.3s ease-out;

      &:hover {
        background-color: $red;
        color: $white;
      }
    }

    .call-today {
      margin-right: 20px;

      .phone-number {
        font-size: 30px;
        font-weight: 700;
        margin: 15px 0 0 0;

        a {
          color: $red;
        }

        span {
          font-size: 14px;
          padding-left: 32px;
          display: block;
        }
      }
    }

    .navbar {
      box-shadow: none;

      .navbar-nav {

        .nav-item {
          margin-right: 50px;
        }
      }
    }
  }
</style>

<script>
// import LocaleDropdown from './LocaleDropdown'
// import AuthUserDropdown from './AuthUserDropdown'

export default {
  components: {},

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
