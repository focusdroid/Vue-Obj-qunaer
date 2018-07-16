<template>
  <div class="hello">
    <Header></Header>
  </div>
</template>

<script>
import Header from './components/Header'
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  },
  components: {
    Header
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hello{
    font-size:0.15rem;
}
</style>
