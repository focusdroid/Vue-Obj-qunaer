<template>
  <div class="recommend">
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in weekendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" :alt="item.title">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.title}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    weekendList: Array
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
    padding: .15rem 0;
  }
  .item{
    padding-bottom: .2rem;
    .item-img-wrapper{
      height:0;
      padding-bottom: 37.09%
      overflow: hidden;
      .item-img {
        width:100%;
      }
    }
    .item-info{
      margin-left:.2rem;
      .item-title{
        line-height: .54rem;
        font-size: .30rem;
        ellipsis();
      }
      .item-desc{
        line-height: .4rem;
        color: #ccc;
        font-size: .25rem;
        ellipsis();
      }
    }
  }
</style>
