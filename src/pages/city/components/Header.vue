<template>
    <div class="header">
      <router-link to="/">
        <div class="header-left">
          <span class="iconfont">&#xe624;</span>
        </div>
      </router-link>
      <div class="header-content">城市选择</div>
      <div class="header-right"></div>
    </div>
</template>

<script>
export default {
}
</script>

<style scoped lang="stylus">
@import '../../../assets/varibles.styl'
.header {
  overflow: hidden;
  height: $headerHeight;
  line-height: $headerHeight;
  text-align: center;
  color: #fff;
  background: $bgColor;
  font-size: $fontsize;
  display: flex;
  justify-content: space-between;
  .header-left {
    color: #fff;
    width: .8rem;
    .iconfont {
      font-size: .3rem;
    }
  }
  .header-right {
    width: 10%
  }
}
</style>
