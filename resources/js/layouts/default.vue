<template>
  <div class="main-layout">
    <navbar />

    <router-view />
  </div>
</template>

<style lang="scss">
  .main-layout {
  }
</style>

<script>
import Navbar from '~/components/Navbar'

export default {
  name: 'MainLayout',

  components: {
    Navbar
  }
}
</script>
