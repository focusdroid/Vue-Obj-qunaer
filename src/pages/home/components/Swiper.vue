<template>
    <div class="swiper">
      <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for="(item) in swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl" alt="">
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
export default {
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination', // 显示下面的小圆点
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/dujia_shuqi_banner_20180710.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/anquan_20180716.png'
      }, {
        id: '0003',
        imgUrl: 'https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/20180713_CPM_11053.jpg'
      }]
    }
  }
}
</script>

<style scoped lang="stylus">
  .swiper >>> .swiper-pagination-bullet-active{// >>> 样式穿透
    background-color: #fff;
  }
  .swiper{ // 防止图片加载闪动问题
    width:100%;
    height:0;
    overflow hidden;
    padding-bottom:31.25%;
  }
.swiper-img{
  width: 100%;
}

</style>
