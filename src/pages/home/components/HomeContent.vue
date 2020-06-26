<template>
  <div class="home-content">
    <Row type="flex" justify="center" style="padding: 40px 0">
      <Col span="20">
        <br>
        <h1 style="font-size: 30px;">Hello, welcome {{username}}</h1>
        <p>清风徐来，水波不兴。举酒属客，诵明月之诗，歌窈窕之章</p>
        <br>
        <Button size="large" type="primary">Learn more >></Button>
      </Col>
    </Row>
    <Row type="flex" justify="center" style="padding: 30px 0;">
      <Col span="20">
        <Row>
          <Col :xs="2" :sm="4" :md="6" :lg="8" v-for="heading in headings" :key="heading">
            <Card class="card">
              <br>
              <h2>{{heading}}</h2>
              <br>
              <p style="font-size: 16px;">Donec id dlit non mi prota gravida</p>
              <Button size="small">View details >></Button>
              <br>
              <br>
            </Card>
          </Col>
        </Row>
        
      </Col>
    </Row>
  </div>
</template>

<script>
  export default {
    name: 'HomeContent',
    data () {
      return {
        username: '清风徐来',
        headings: [
          '吃饭',
          '睡觉',
          '打豆豆',
          '辣条',
          '火锅',
          '雪碧'
        ]
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .card {
    background: #fbfbfb;
    display: inline-block;
    margin: 0.3em;
    border-radius: 20px;
    box-shadow: 5px 5px 5px #ccc;
  }
</style>