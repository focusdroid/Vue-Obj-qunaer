<template>
  <div class="recommend">
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" :alt="item.title">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.title}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    recommendList: Array
  },
  data () {
    return {
    }
  }
}
</script>

<style scoped lang="stylus">
  @import '../../../../static/css/mixin.styl' // 控制样式一行显示
.title{
  line-height:.4rem;
  background: #eee;
  text-indent: .2rem;
  font-size: .25rem;
  margin-top: .2rem;
  padding: .15rem 0;
}
  .item{
    display:flex;
    height: 1.9rem;
    overflow: hidden;
    margin-top: .2rem;
    padding-bottom: .2rem;
    .item-img-wrapper{
      padding:.1rem;
      .item-img {
        width: 1.7rem;
        height: 1.7rem;
        -webkit-border-radius: 5px;
        -moz-border-radius: 5px;
        border-radius: 5px;
      }
    }
    .item-info{
      flex: 1;
      padding: .1rem;
      min-width:0; // 关键的一行显示样式生效的代码
      .item-title{
        line-height: .54rem;
        font-size: .32rem;
        ellipsis();
      }
      .item-desc{
        line-height: .4rem;
        color: #ccc;
        font-size: .25rem;
        ellipsis();
      }
      .item-button{
        margin-top: .2rem;
        background: #ff9300;
        padding: 0 .15rem;
        border-radius: .06rem;
        color: #fff;
        line-height: .44rem;
      }
    }
  }
</style>
