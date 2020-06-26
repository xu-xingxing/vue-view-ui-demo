<template>
  <div id="app">
  <!-- <login></login> -->
    <home></home>
  </div>
</template>

<script>
import Login from './pages/login/Login'
import Home from './pages/home/Home'
export default {
  name: 'App',
  components: {
    Login,
    Home
  }
}
</script>

<style>

</style>
