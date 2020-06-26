<template>
  <div>
    <home-header></home-header>
    <home-content></home-content>
    <home-bottom></home-bottom>
  </div>
</template>

<script>
  import HomeHeader from './components/HomeHeader'
  import HomeContent from './components/HomeContent'
  import HomeBottom from './components/HomeBottom'
  export default {
    name: 'Home',
    components: {
      HomeHeader,
      HomeContent,
      HomeBottom
    }
  }
</script>

<style lang="scss" scoped>

</style>