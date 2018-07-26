<template>
  <div class="search">
    <input type="text" class="search-input" placeholder="输入城市名或拼音">
  </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="stylus">
@import '../../../assets/varibles.styl'
  .search{
    height:.72rem;
    padding: .1rem;
    background:$bgColor;
    .search-input {
      box-sizing: border-box;//防止加padding之后出现过宽
      width:100%;
      height: .62rem;
      line-height: .62rem;
      text-align:center;
      border-radius: .06rem;
      color: #666;
      padding: 0 .1rem;
    }
  }
</style>
