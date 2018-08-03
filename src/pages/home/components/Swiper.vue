<!-- The ref attr used to find the swiper instance -->
<template>
  <div class="swiper-div">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HeaderSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/c6/44fce1467be17702.jpg_750x200_406f5fc3.jpg'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/3c/c72a1ccd4d7b2202.jpg_750x200_b88bbab4.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  /**.swiper-pagination-bullet-active其实是<swiper>组件内的样式，当前页面为HeaderSwiper组件 其样式受scoped限制，因此不能使用<swiper>组件内的样式
  解决方法  使用 >>> 进行样式穿透 意思是.swiper-pagination-bullet-active样式适用于当前页
  **/
  .swiper-div >>> .swiper-pagination-bullet-active
    background-color: #fff;
  .swiper-div
    overflow: hidden
    width: 100
    height: 0
    padding-bottom: 26.67%
    background-color: #eee
    .swiper-img
      width: 100%;
</style>
