<template>
    <div>
      <ul class="list">
        <li
          class="item"
          v-for="(item, key) in cities"
          :key="item.id"
          @click="heandler"
        >{{key}}</li>
      </ul>
    </div>
</template>

<script>
export default {
  props: {
    cities: Object
  },
  methods: {
    heandler (e) {
      this.$emit('change', e.target.innerText)
    }
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
