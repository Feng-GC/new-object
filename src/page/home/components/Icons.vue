<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of swiperList" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-l" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeIcons",
  props:{
    iconsList:Array
  },
  data() {
    return {
      // imgList: [
      //   {
      //     id: "001",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "002",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "003",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "004",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "005",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "006",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "007",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "008",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "009",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "0010",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   },
      //   {
      //     id: "011",
      //     url:
      //       "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
      //     des: "热门景点"
      //   }
      // ],
      swiperOption:{
        autoplay:false,
        
      }
    };
  },
  computed: {
    swiperList: function() {
      var listArr = [];
      console.log(this.iconsList)
      this.iconsList.forEach((item, index) => {
        var page = Math.floor(index / 10);
        if(!listArr[page]){
          listArr[page] = []
        }
        listArr[page].push(item)
      });
      return listArr
    }
  }
};
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl';

.icons {
  overflow: hidden;
  height: 0;
  padding-bottom: 40%;
  margin-top 0.28rem;
  .icon {
    overflow: hidden;
    width: 20%;
    height: 0;
    float: left;
    padding-bottom: 20%;
    position: relative;

    .icon-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44rem;
      box-sizing: border-box;
      padding: 0.1rem;

      .icon-img-l {
        height: 100%;
        display: block;
        margin: 0 auto;
      }
    }

    .icon-desc {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      color: #333;
      line-height: 0.44rem;
      color: $blackColor;
      text-align: center;
    }
  }
}
</style>

