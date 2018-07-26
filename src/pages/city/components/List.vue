<template>
  <div class="lists" ref="wrapper" id="wrapper">
    <div >

    </div>
    <div class="area">
      <div class="title border-topbottom">当前城市</div>
      <div class="button-list">
        <div class="button-wrapper">
          <div class="button">北京</div>
          <div class="button">北京</div>
          <div class="button">北京</div>
          <div class="button">北京</div>
          <div class="button">北京</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">热门城市</div>
      <div class="button-list">
        <div class="button-wrapper">
          <div class="button">北京</div>
          <div class="button">北京</div>
          <div class="button">北京</div>
          <div class="button">北京</div>
          <div class="button">北京</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
      </div>
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
      </div>
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
        <div class="item border-bottom">阿拉善</div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  }
}
</script>

<style scoped lang="stylus">
@import '../../../assets/varibles.styl'
.border-topbottom{
  &:before{// 控制一像素边框的样式
    border-color: #ccc;
  }
  &:after{
    border-color: #ccc;
  }
}
  .border-bottom{
    &:before{
      border-color: #ccc;
    }
  }
    .wrapper{
      height:100%
    }
    .list{
      position: absolute;
      top:1.78rem
      left:0
      bottom:0
      right:0
    }
  .title{
    line-height: .54rem;
    background-color: #eee;
    padding-left:.2rem;
    font-size:.26rem;
  }
  .button-list{
    overflow: hidden;
    padding: .1rem;
    .button-wrapper{
      .button{
        margin: .1rem;
        padding: .1rem 0;
        border-radius: 0.1rem;
        text-align: center;
        border: .02rem solid #ccc;
        width: 30%;
        float: left;
      }
    }
  }
  .item-list{
    .item{
      line-height: .6rem
      padding-left: .2rem
    }
  }
</style>
