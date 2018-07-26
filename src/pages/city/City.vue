<template>
    <div class="city">
      <Header></Header>
      <Search></Search>
      <List></List>
      <Alphabet></Alphabet>
    </div>
</template>

<script>
import Header from './components/Header'
import Search from './components/Search'
import List from './components/List'
import Alphabet from './components/Alphabet'
export default {
  components: {
    Header,
    Search,
    List,
    Alphabet
  }
}
</script>

<style scoped lang="stylus">

</style>
