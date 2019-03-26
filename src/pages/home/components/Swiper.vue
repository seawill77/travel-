<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
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
        imgUrl: 'https://img.alicdn.com/tfs/TB1zJJ3BrvpK1RjSZPiXXbmwXXa-700-255.png'
      }, {
        id: '002',
        imgUrl: 'https://img.alicdn.com/tfs/TB10cR9BwHqK1RjSZFEXXcGMXXa-700-255.png'
      }, {
        id: '003',
        imgUrl: 'https://img.alicdn.com/imgextra/i1/2466144055/O1CN011BUae51fpEXmbQC9B_!!2466144055.jpg'
      }]
    }
  }
}

</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-activ
     background: #fff
    .wrapper
      overflow: hidden
      width: 100%
      height: 0
      padding-bottom: 31.25%
   .swiper-pagination-bullet-activ
      background: red !important
   .swiper-img
     width: 100%

</style>
