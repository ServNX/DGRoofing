<template>
  <header class="header">
    <div class="top-bar">
      <b-container>
        <b-row class="justify-content-md-center">
          <b-col lg="5">
            <div class="topbar-col-1">
              <div class="phone-number">
                <fa icon="phone" class="text-dark" />
                <a href="tel:1-937-439-0554">937-439-0554</a>
              </div>
              <span>Call today for a free estimate.</span>
            </div>
          </b-col>
          <b-col lg="2">
            <b-img class="logo" src="dist/img/logo.png" alt="D & G Roofing Logo" fluid />
          </b-col>
          <b-col lg="5" class="d-flex justify-content-end">
            <b-button variant="outline-danger">
              Get A Free Estimate
            </b-button>
          </b-col>
        </b-row>
      </b-container>
    </div>

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

  .header {
    position: relative;
    z-index: 15;

    .top-bar {
      .logo {
        padding: 10px 0 10px 0;
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
        -webkit-transition: all 0.3s ease-out;
        -moz-transition: all 0.3s ease-out;
        -ms-transition: all 0.3s ease-out;
        -o-transition: all 0.3s ease-out;
        transition: all 0.3s ease-out;

        &:hover {
          background-color: $red;
          color: $white;
        }
      }

      .phone-number {
        font-size: 30px;
        font-weight: 700;
        margin: 45px 0 0 0;

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
      border-bottom: 1px solid $red;

      .navbar-nav {

        .nav-item {
          margin-right: 50px;

          &:hover {
            .nav-link {
              color: $white;
            }
          }
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
