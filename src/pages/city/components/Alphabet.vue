<template>
    <div>
      <ul class="list">
        <li class="item" v-for="(item, key) in cities" :key="item.id">{{key}}</li>
      </ul>
    </div>
</template>

<script>
export default {
  props: {
    cities: Object
  }
}
</script>

<style scoped lang="stylus">
@import '../../../assets/varibles.styl'
  .list{
    position: fixed
    top:3.3rem
    right:0
    width: .4rem
    display: flex
    flex-direction: column
    justify-content: center
    .item {
      line-height: .4rem
      text-align: center
      color: $bgColor
    }
  }
</style>
