<template>
    <div class="icons">
        <swiper :options="swiperOption">
            <swiper-slide v-for="(page,index) in pages" :key="index">
                <div class="icon" v-for="item in page" :key="item.id">
                    <div class="icon-img">
                        <img class="img" :src="item.imgUrl" />
                    </div>
                    <p class="icon-desc">{{item.desc}}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
  data() {
    return {
      swiperOption: {
        autoplay: 0
      },
      iconList: [
        {
          id: 1,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: 2,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: 3,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: 4,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: 5,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: 6,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: 7,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: 8,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: 9,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: 10,
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        }
      ]
    };
  },
  computed: {
    pages() {
      let pages = [];
      this.iconList.forEach(function(item, index) {
        var page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item);
      });
      return pages;
    }
  },
  components: {}
};
</script>

<style scoped>
.icons {
  width: 100%;
  height: 0;
  padding-bottom: 50%;
}
.icon {
  overflow: hidden;
  float: left;
  width: 25%;
  height: 0;
  padding-bottom: 25%;
  position: relative;
}
.icon-img {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0.44rem;
  display: flex;
  align-items:center;
}
.icon-img .img {
  display: block;
  height: 80%;
  margin: 0 auto;
}
.icon-desc {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 0.44rem;
  line-height: 0.44rem;
  color: #333;
  text-align: center;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
</style>
