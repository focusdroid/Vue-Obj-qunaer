<template>
    <div>
      <ul class="list">
        <li class="item">A</li>
        <li class="item">A</li>
        <li class="item">A</li>
        <li class="item">A</li>
        <li class="item">A</li>
        <li class="item">A</li>
        <li class="item">A</li>
      </ul>
    </div>
</template>

<script>
export default {
}
</script>

<style scoped lang="stylus">
@import '../../../assets/varibles.styl'
  .list{
    position: fixed
    top: 1.78rem
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
