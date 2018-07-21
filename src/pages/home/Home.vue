<template>
  <div class="hello">
    <Header></Header>
    <HomeSwiper></HomeSwiper>
    <Icons></Icons>
    <Recommend></Recommend>
  </div>
</template>

<script>
import Header from './components/Header'
import HomeSwiper from './components/Swiper'
import Icons from './components/Icons'
import Recommend from './components/Recommend'
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  },
  components: {
    Header,
    HomeSwiper,
    Icons,
    Recommend
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hello{
    font-size:0.15rem;
}
</style>
