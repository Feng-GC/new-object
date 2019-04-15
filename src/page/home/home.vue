<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    <home-gowhere></home-gowhere>
  </div>
</template>

<script>
import HomeHeader from "./components/header";
import HomeSwiper from "./components/Swiper";
import HomeIcons from "./components/Icons";
import HomeRecommend from "./components/recommend";
import HomeGowhere from './components/gowhere'

export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeGowhere,
  }
};
</script>

<style>
</style>
