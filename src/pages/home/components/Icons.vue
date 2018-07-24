<template>
  <div class="icons">
    <div class="icon">
      <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for="(temp, i) in pages" :key="i">
          <ul>
            <li v-for="item in temp" :key="item.id">
              <a :href="item.linkUrl">
                <img :src="item.imgUrl" :alt="item.desc">
                <p>{{item.desc}}</p>
              </a>
            </li>
          </ul>
        </swiper-slide>
        <!--<swiper-slide>
          <ul>
            <li v-for="item in iconList.slice(8,iconList.length)" :key="item.id">
              <a :href="item.linkUrl">
                <img :src="item.imgUrl" :alt="item.desc">
                <p>{{item.desc}}</p>
              </a>
            </li>
          </ul>
        </swiper-slide>-->
        <!--&lt;!&ndash; Optional controls &ndash;&gt;-->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>

    </div>
  </div>
</template>

<script>
export default {
  props: {
    iconList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: false
      }
    }
  },
  computed: {
    pages () { // 计算轮播图的分页，按照页码显示轮播图页数
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style scoped lang="stylus">
  swiper-pagination
  icons >>> .swiper-pagination-bullet {
    marign-bottom:.01rem;
  }
   .icons >>> .swiper-pagination-bullet-active{
     background: rgba(0,175,190,.8);
   }
.icons {
  height:110%;
  .icon {
    height:110%;
    ul {
      display:flex;
      width:100%;
      flex-wrap: wrap;
      li{
        width:25%;
        text-align: center;
        line-height:.5rem;
        margin-top:.2rem;
        img{
          width: 1.1rem;
          height: 1.1rem;
        }
        p{
          font-size:0.25rem;
          color: #212121;
        }
      }
    }
  }
}
</style>
