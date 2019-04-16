<template>
  <div>
    <home-header :city="cityData"></home-header>
    <home-swiper :swiperList="swiperData"></home-swiper>
    <home-icons :iconsList="iconsData"></home-icons>
    <home-recommend :recommendList="recommendData"></home-recommend>
    <home-gowhere :goWhereList="gowhereData"></home-gowhere>
  </div>
</template>

<script>
import HomeHeader from "./components/header";
import HomeSwiper from "./components/Swiper";
import HomeIcons from "./components/Icons";
import HomeRecommend from "./components/recommend";
import HomeGowhere from "./components/gowhere";
import axios from "axios";

export default {
  name: "Home",
  data() {
    return {
      cityData: "",
      swiperData: [],
      iconsData: [],
      recommendData: [],
      gowhereData: []
    };
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeGowhere
  },
  methods: {
    getHomeInfo() {
      axios.get("/api/index.json").then(this.getHomeInfoSucc);
    },
    getHomeInfoSucc(res) {
      res = res.data;

      if (res.ret && res.data) {
        var datas = res.data;
        this.cityData = datas.city;
        this.swiperData = datas.swiperList;
        this.iconsData = datas.iconList;
        this.recommendData = datas.recommendList;
        this.gowhereData = datas.weekendList;
      }
    }
  },

  mounted() {
    this.getHomeInfo();
  }
};
</script>

<style>
</style>
