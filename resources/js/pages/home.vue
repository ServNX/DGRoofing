<template>
  <div>
    <home-header />

    <why-choose-us />

    <services />
  </div>
</template>

<style lang="scss" scoped>

</style>

<script>
import HomeHeader from '../components/headers/HomeHeader'
import WhyChooseUs from '../components/sections/WhyChooseUs'
import Services from '../components/sections/Services'

export default {
  components: {
    Services,
    HomeHeader,
    WhyChooseUs
  }
}
</script>
