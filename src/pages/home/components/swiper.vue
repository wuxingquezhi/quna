<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item in swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" />
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  data() {
    return {
      swiperOption: {
        loop: true,
        pagination: ".swiper-pagination"
      },
      swiperList:[
          {id:'1',imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/dd/269c3dafd51a2502.jpg_750x200_4fb86e3e.jpg'},
          {id:'2',imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/ba/5a7899d201e21602.jpg_750x200_0cf5f940.jpg'}
      ]
    };
  },
  components: {}
};
</script>

<style scoped>
.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 26.666%;
  background: #eee;
}
.swiper-img {
  width: 100%;
}

.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}
</style>
