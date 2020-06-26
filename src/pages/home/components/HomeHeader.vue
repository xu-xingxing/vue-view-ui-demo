<template>
  <div class="home-header">
    <Row type="flex" justify="center" style="background: #409eff;font-size: 15px;padding: 8px 0 10px 0;">
      <Col span="20">
        <h1 style="color: #fff;">{{title}}</h1>
      </Col>
    </Row>
  </div>
</template>

<script>
  export default {
    name: 'HomeHeader',
    data () {
      return {
        title: '清风徐来后台管理系统'
      }
    }
  }
</script>

<style lang="stylus" scoped>

</style>