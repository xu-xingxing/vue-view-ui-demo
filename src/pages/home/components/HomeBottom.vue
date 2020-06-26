<template>
  <div class="home-bottom">
    <Row type="flex" justify="center" style="padding: 20px 0">
      <Col span="20">
        <p style="color: #409eff;text-align: center;">@{{copyRight}}</p>
      </Col>
    </Row>
  </div>
</template>

<script>
  export default {
    name: 'HomeBottom',
    data () {
      return {
        copyRight: 'copyright 2020年06月26日'
      }
    }
  }
</script>

<style lang="stylus" scoped>

</style>