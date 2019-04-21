<template>
  <div>
    <city-header></city-header>
    <city-search :city='alphabetData'></city-search>
    <city-list :listDatas="listData" :alphabetDatas="alphabetData" :letters="letter"></city-list>
    <city-alphabet 
      :alphabetDatas="alphabetData"
      @change="handleLetterChange"
    ></city-alphabet>
  </div>
</template>

<script>
import CityHeader from './components/cityHeader'
import CityList from './components/cityList';
import CitySearch from './components/citySearch';
import CityAlphabet from './components/cityalphabet'
import  axios from "axios";

export default {
  name:'City',
  data(){
    return{
      listData:[],
      alphabetData:{},
      letter:'',
    }
  },
  components:{
    CityHeader:CityHeader,
    CityList,
    CitySearch,
    CityAlphabet
  },
  methods:{
    getCityinfo(){
      axios.get("/api/city.json").then(this.getCityinfoSucc)
    },
    getCityinfoSucc(res){
      res = res.data
      var data = res.data

      if (res.ret && res.data){
        
        this.listData = res.data.hotCities;
        this.alphabetData = res.data.cities
      }
    },
    handleLetterChange(letters){
      
      this.letter = letters
      
    }
  },
  mounted(){
    this.getCityinfo()
  }
}
</script>

<style>
</style>
