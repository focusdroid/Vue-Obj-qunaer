<template>
  <div class="recommend">
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommentList" :key="item.id">
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
  data () {
    return {
      recommentList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg',
          title: '华清爱琴海温泉',
          desc: '华清爱琴海温泉'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1507/98/d9c848b0d7d65a.jpg_r_640x214_55778a01.jpg',
          title: '曲江海洋极地公园',
          desc: '曲江海洋极地公园'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1507/de/e6ba44d61894c0.jpg_r_640x214_847324d0.jpg',
          title: '长恨歌',
          desc: '长恨歌'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1511/14/1cf5dc2ecbfc16.jpg_r_640x214_b4b3a58a.jpg',
          title: '华清宫（华清池·骊山）(5A)',
          desc: '华清宫（华清池·骊山）(5A)'
        }
      ]
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
      padding-bottom: 33.9%
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
