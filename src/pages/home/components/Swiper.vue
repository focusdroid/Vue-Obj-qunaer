<template>
    <div class="swiper">
      <swiper :options="swiperOption" v-if="showSeiper">
        <!-- slides -->
        <swiper-slide v-for="(item) in list" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl" alt="">
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
export default {
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination', // 显示下面的小圆点
        loop: true
      }
    }
  },
  computed: {
    showSeiper () {
      return this.list.length
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
    padding-bottom:24.5%;
  }
.swiper-img{
  width: 100%;
}

</style>
