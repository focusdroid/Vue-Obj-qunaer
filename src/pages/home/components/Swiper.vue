<template>
    <div class="swiper">
      <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide>
          <img class="swiper-img" src="https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/dujia_shuqi_banner_20180710.jpg" alt="">
        </swiper-slide>
        <swiper-slide>
          <img class="swiper-img" src="https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/20180713_CPM_11053.jpg" alt="">
        </swiper-slide>
        <swiper-slide>
          <img class="swiper-img" src="https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/anquan_20180716.png" alt="">
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
      swiperOption:{ }
    }
  }
}
</script>

<style scoped>
.swiper-img{
  width: 100%;
}
</style>
