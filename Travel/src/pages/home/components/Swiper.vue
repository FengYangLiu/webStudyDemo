<template>
<div class="wrapper">
  <swiper :options="swiperOption">
  <swiper-slide v-for="item of swiperList" :key="item.id">
  <img class="swiper-img" :src="item.imgUrl" alt="" />
  </swiper-slide>
  <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '001',
        imgUrl: 'https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/dujia_shuqi_banner_20180710.jpg'
      },
      {
        id: '002',
        imgUrl: 'https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/20180713_CPM_11053.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}

.wrapper {
  width: 100%;
  height: 0;
  overflow: hidden;
  padding-bottom: 24.53%;

  .swiper-img {
    width: 100%;
  }
}
</style>
