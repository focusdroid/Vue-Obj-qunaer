<template>
  <div class="hello">
    <Header :city="city"></Header>
    <HomeSwiper :list="swiperList"></HomeSwiper>
    <Icons :iconList="iconList"></Icons>
    <Recommend :recommendList="recommendList"></Recommend>
    <Weekend :weekendList="weekendList"></Weekend>
  </div>
</template>
<script>
import Header from './components/Header'
import HomeSwiper from './components/Swiper'
import Icons from './components/Icons'
import Recommend from './components/Recommend'
import Weekend from './components/Weekend'

import axios from 'axios'
export default {
  name: 'HelloWorld',
  data () {
    return {
      city: '',
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  components: {
    Header,
    HomeSwiper,
    Icons,
    Recommend,
    Weekend
  },
  mounted () {
    this.getHomeInfo()
  },
  methods: {
    getHomeInfo () {
      axios.get('api/index.json').then((res) => {
        if (res.data.ret) {
          this.city = res.data.city
          this.swiperList = res.data.data.swiperList
          this.iconList = res.data.data.iconList
          this.recommendList = res.data.data.recommendList
          this.weekendList = res.data.data.weekendList
        }
      }).then()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hello{
    font-size:0.15rem;
}
</style>
