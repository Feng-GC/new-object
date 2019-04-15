<template>
  <div class="recommend">
    <div class="like-you">
      <span class="iconfont heart">&#xe600;</span>猜你喜欢
    </div>
    <ul class="ul">
      <li v-for="item of listArr" :key="item.id">
        <div class="left">
          <img :src="item.imgurl">
        </div>
        <div class="right">
          <div>
            <div class="title">{{item.title}}</div>
            <div class="start-content">
              <strong class="iconfont start">&#xe601;</strong>
              103556条评论
            </div>
            <div class="price-content">
              <span>
                <span style="color:#FF8300">￥</span>
                <span class="price">{{item.price}}</span>起
                <span class="price-right">{{item.adderss}}</span>
              </span>
            </div>
            <div class="tips" v-show="item.tips">{{item.tipsDsc}}</div>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  data() {
    return {
      listArr: [
        {
          id: "001",
          imgurl:
            "http://img1.qunarzz.com/sight/p0/201403/07/30b534b0de51ccac2906bcb6ba159988.jpg_200x200_2f08733b.jpg",
          title: "长隆野生动物世界",
          start: "5",
          price: "220.1",
          adderss: "广州长隆",
          tips: true,
          tipsDsc: "熊猫三胞胎与您共享欢乐时光"
        },
        {
          id: "002",
          imgurl:
            "http://img1.qunarzz.com/sight/p0/201403/07/30b534b0de51ccac2906bcb6ba159988.jpg_200x200_2f08733b.jpg",
          title: "长隆野生动物世界",
          start: "5",
          price: "220.1",
          adderss: "广州长隆",
          tips: false
        },
        {
          id: "003",
          imgurl:
            "http://img1.qunarzz.com/sight/p0/201403/07/30b534b0de51ccac2906bcb6ba159988.jpg_200x200_2f08733b.jpg",
          title: "长隆野生动物世界",
          start: "5",
          price: "220.1",
          adderss: "广州长隆",
          tips: true,
          tipsDsc: "熊猫三胞胎与您共享欢乐时光"
        },
        {
          id: "004",
          imgurl:
            "http://img1.qunarzz.com/sight/p0/201403/07/30b534b0de51ccac2906bcb6ba159988.jpg_200x200_2f08733b.jpg",
          title: "长隆野生动物世界",
          start: "5",
          price: "220.1",
          adderss: "广州长隆",
          tips: true,
          tipsDsc: "熊猫三胞胎与您共享欢乐时光"
        },
        {
          id: "005",
          imgurl:
            "http://img1.qunarzz.com/sight/p0/201403/07/30b534b0de51ccac2906bcb6ba159988.jpg_200x200_2f08733b.jpg",
          title: "长隆野生动物世界",
          start: "5",
          price: "220.1",
          adderss: "广州长隆",
          tips: false,
          tipsDsc: "熊猫三胞胎与您共享欢乐时光"
        },{
          id: "006",
          imgurl:
            "http://img1.qunarzz.com/sight/p0/201403/07/30b534b0de51ccac2906bcb6ba159988.jpg_200x200_2f08733b.jpg",
          title: "长隆野生动物世界",
          start: "5",
          price: "220.1",
          adderss: "广州长隆",
          tips: false,
          tipsDsc: "熊猫三胞胎与您共享欢乐时光"
        },
      ]
    };
  },
  computed: {
    strarNum: function() {
      var startFont = "&#xe601;";
      var startNums = "";
      for (var i = 0; i < 5; i++) {
        startNums += startFont;
      }
      console.log(startNums);
      return startNums;
    }
  }
};
</script>


<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl';

.recommend {
  width: 100%;
  
  .like-you {
    height: 0.44rem;
    line-height: 0.44rem;
    text-shadow: 0 0 balck;
    font-size: 0.32rem;
    padding: 0.24rem 0.26rem;

    .heart {
      color: red;
      text-shadow: 0 0 red;
      margin-right: 0.09rem;
    }
  }

  .ul li {
    padding: 0.1rem 0;
    overflow: hidden;
    margin-top: 0.1rem;
    margin-bottom: 0.2rem;

    .left {
      overflow: hidden;
      height: 2rem;
      width: 2rem;
      float: left;
      margin-right: 0.2rem;

      img {
        width: 100%;
      }
    }

    .right {
      overflow: hidden;
    }

    .title {
      padding-top: 0.26rem;
      color: $blackColor;
      font-size: 0.32rem;
      height: 0.44rem;
      line-height: 0.44rem;
    }

    .start-content {
      height: 0.34rem;
      line-height: 0.34rem;
      padding-top: 0.14rem;
      font-size: 0.12rem;

      .start {
        color: $yellowColor;
        font-size: 0.24rem;
        overflow: hidden;
      }
    }

    .price-content {
      padding-top: 0.22rem;
      position: relative;
      font-size: 0.24rem;

      .price {
        line-height: 0.4rem;
        font-size: 0.4rem;
        color: $organColor;
      }

      .price-right {
        position: absolute;
        right: 0.1rem;
        bottom: 0;
      }
    }

    .tips {
      margin-top: 0.34rem;
      padding: 0.04rem 0.1rem;
      background: #fff9f9;
      line-height: 0.34rem;
      color: #FF5555;
      font-size: 0.24rem;
      line-height: 0.34rem;
    }
  }
}
</style>
