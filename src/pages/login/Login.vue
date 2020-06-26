<template>
  <div id="login" style="background: #eee;">
    <login-top></login-top>
    <login-content></login-content>
  </div>
</template>

<script>
  import LoginTop from './components/LoginTop'
  import LoginContent from './components/LoginContent'
  export default {
    name: 'Login',
    components: {
      LoginTop,
      LoginContent
    }
  }
</script>

<style lang="stylus" scoped>

</style>