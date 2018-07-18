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
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票',
        linkUrl: 'https://touch.piao.qunar.com/touch/list_北京_景点门票.html?cat=from_area%3Dts_type_nav%26from_index%3D0%26from_value%3D%25E6%2599%25AF%25E7%2582%25B9%25E9%2597%25A8%25E7%25A5%25A8%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        desc: '北京必游',
        linkUrl: 'https://sale.piao.qunar.com/touch/topic/mk/t_2927.htm?cat=from_area%3Dts_type_nav%26from_index%3D1%26from_value%3D%25E5%258C%2597%25E4%25BA%25AC%25E5%25BF%2585%25E6%25B8%25B8%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png',
        desc: '夏日玩水',
        linkUrl: 'https://touch.piao.qunar.com/touch/list_北京_水上乐园.html?cat=from_area%3Dts_type_nav%26from_index%3D2%26from_value%3D%25E5%25A4%258F%25E6%2597%25A5%25E7%258E%25A9%25E6%25B0%25B4%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      },
      {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        desc: '文化古迹',
        linkUrl: 'https://touch.piao.qunar.com/touch/list_北京_文化古迹.html?cat=from_area%3Dts_type_nav%26from_index%3D3%26from_value%3D%25E6%2596%2587%25E5%258C%2596%25E5%258F%25A4%25E8%25BF%25B9%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      },
      {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        desc: '动植物园',
        linkUrl: 'https://touch.piao.qunar.com/touch/list_北京_动植物园.html?cat=from_area%3Dts_type_nav%26from_index%3D4%26from_value%3D%25E5%258A%25A8%25E6%25A4%258D%25E7%2589%25A9%25E5%259B%25AD%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      },
      {
        id: '0006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
        desc: '故宫',
        linkUrl: 'http://sale.piao.qunar.com/touch/topic/mk/t_1135.htm?cat=from_area%3Dts_type_nav%26from_index%3D5%26from_value%3D%25E6%2595%2585%25E5%25AE%25AB%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      },
      {
        id: '0007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        desc: '一日游',
        linkUrl: 'http://touch.piao.qunar.com/touch/list.htm?limitCondition=oneDayTour&region=北京&cityName=北京&keyword=一日游&cat=from_area%3Dts_type_nav%26from_index%3D6%26from_value%3D%25E4%25B8%2580%25E6%2597%25A5%25E6%25B8%25B8%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      },
      {
        id: '0008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png',
        desc: '公园',
        linkUrl: 'https://touch.piao.qunar.com/touch/list_北京_公园.html?cat=from_area%3Dts_type_nav%26from_index%3D7%26from_value%3D%25E5%2585%25AC%25E5%259B%25AD%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      },
      {
        id: '0009',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
        desc: '游乐场',
        linkUrl: 'https://touch.piao.qunar.com/touch/list_北京_游乐场.html?cat=from_area%3Dts_type_nav%26from_index%3D8%26from_value%3D%25E6%25B8%25B8%25E4%25B9%2590%25E5%259C%25BA%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      },
      {
        id: '0010',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',
        desc: '全部玩乐',
        linkUrl: 'https://touch.piao.qunar.com/touch/list_北京_全部玩乐.html?cat=from_area%3Dts_type_nav%26from_index%3D9%26from_value%3D%25E5%2585%25A8%25E9%2583%25A8%25E7%258E%25A9%25E4%25B9%2590%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
      }],
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
