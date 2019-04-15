<template>
  <div class="gowhere">
    <div class="title">周未去哪里</div>
    <div class="all" v-for="item of listArr" :key="item.id">
      <div class="img-content">
        <img :src="item.imgUrl">
      </div>
      <div class="content">
        <div class="titles">{{item.title}}</div>
        <div class="text">{{item.text}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Homegowhere",
  data: function() {
    return {
      listArr: [
        {
          id: "001",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg",
          title: "清远周边逛",
          text:
            "人人都有一双发现美的眼睛，身边的事物最熟悉不过，那你可曾发现了被人遗漏的美？"
        },
        {
          id: "002",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg",
          title: "清远周边逛",
          text:
            "人人都有一双发现美的眼睛，身边的事物最熟悉不过，那你可曾发现了被人遗漏的美？"
        },
        {
          id: "003",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1505/92/580e9ea4f37a1b.jpg_r_640x214_72112761.jpg",
          title: "清远周边逛",
          text:
            "人人都有一双发现美的眼睛，身边的事物最熟悉不过，那你可曾发现了被人遗漏的美？"
        },
        {
          id: "004",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1811/f8/29dfa785277839.jpg_r_640x214_7d051523.jpg",
          title: "清远周边逛",
          text:
            "人人都有一双发现美的眼睛，身边的事物最熟悉不过，那你可曾发现了被人遗漏的美？"
        }
      ]
    };
  }
};
</script>

 <style lang="stylus" scoped>
 .gowhere {
   width: 100%;

   .title {
     height: 0.8rem;
     padding: 0.26rem;
     line-height: 0.8rem;
     background: rgb(245 245 245);
   }

   .all {
     margin-bottom 0.48rem 
     .img-content {
       overflow: hidden;
       height: 0;
       padding-bottom: 37.4375%;

       img {
         width: 100%;
       }
     }

     .content {
       margin-top:0.28rem 
       padding-left 0.28rem
       .titles {
         padding: right 1.4rem;
         font-size: 0.28rem;
         line-height: 0.48rem;
         white-space: norwrap;
         text-emphasis: ellipsis;
       }

       .text {
         padding: right 1.4rem;
         font-size: 0.22rem;
         line-height: 0.48rem;
         white-space: norwrap;
         text-emphasis: ellipsis;
         background rgb(245 245 245)
       }
     }
   }
 }
</style>


