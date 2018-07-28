<template>
    <div class="city">
      <Header></Header>
      <Search></Search>
      <List :cities="cities" :hotCities="hotCities"></List>
      <Alphabet :cities="cities" ></Alphabet>
    </div>
</template>

<script>
import axios from 'axios'
import Header from './components/Header'
import Search from './components/Search'
import List from './components/List'
import Alphabet from './components/Alphabet'
export default {
  data () {
    return {
      cities: {},
      hotCities: []
    }
  },
  components: {
    Header,
    Search,
    List,
    Alphabet
  },
  mounted () {
    this.getCityInfo()
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json').then((res) => {
        console.log(res)
        if (res.data.ret) {
          this.cities = res.data.data.cities
          this.hotCities = res.data.data.hotCities
        }
      })
    }
  }
}
</script>

<style scoped lang="stylus">

</style>
