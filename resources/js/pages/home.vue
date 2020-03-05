<template>
  <b-jumbotron header="BootstrapVue" lead="Bootstrap v4 Components for Vue.js 2">
    <p>For more information visit our website</p>
    <b-button variant="primary" href="https://bootstrap-vue.js.org/">
      More Info
    </b-button>
  </b-jumbotron>
</template>

<script>
import { BJumbotron, BButton } from 'bootstrap-vue'

export default {
  components: {
    BJumbotron,
    BButton
  }
}
</script>
