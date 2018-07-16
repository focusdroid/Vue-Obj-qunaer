<template>
    <div class="header">
      <div class="header-left">
        <span class="iconfont">&#xe624;</span>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/经典/主题
        <!--<input type="text">-->
      </div>
      <div class="header-right">城市 <span class="iconfont">&#xe64a;</span></div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      age: 12
    }
  }
}
</script>

<style scoped lang="stylus">
  /*@import '../../../assets/varibles.styl'*/
  @import '~@/assets/varibles.styl'
.header {
  display: flex;
  height: 0.86rem;
  font-size: 0.3rem;
  background: $bgColor;
  color: #fff;
  line-height 0.86rem;
  font-size:.28rem;
  .header-left {
    width: 0.8rem;
    float: left;
    text-align center;
  }
  .header-input{
    flex: 1;
    background #fff;
    -webkit-border-radius: 0.1rem;
    -moz-border-radius: 0.1rem;
    border-radius: 0.1rem;
    margin-top:0.12rem;
    height: 0.64rem;
    margin-left:.2rem;
    color: #ccc;
    line-height:.64rem;
    font-size:.25rem;
    padding-left:.1rem;
  }
  .header-right {
    width: 1.24rem;
    float right;
    text-align center;
    span{
      font-size .24rem;
    }
  }
}
</style>
