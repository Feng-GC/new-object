<template>
  <div class="wrapper" >
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of imgList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" >
      </swiper-slide>
      
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  data: function() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination",
        loop:true
      },
      imgList:[
        {
          id:'01',
          imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/389d0194766566f8f1185aa19b759c25.jpg_750x200_22620261.jpg'
        },{
          id:'02',
          imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/170b7a4be860098fca27e8b36b92da8a.jpg_750x200_002237e3.jpg'
        },{
          id:'03',
          imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/eb47a432471be6ac40b69828676479dd.jpg_750x200_207de9c6.jpg'
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}

.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 26.71%;
  background: #eeeeee;

  .swiper-img {
    width: 100%;
  }
}
</style>

