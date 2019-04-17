<template>
  <div>
    <city-header></city-header>
    <city-list></city-list>
  </div>
</template>

<script>
import CityHeader from './components/cityHeader'
import CityList from './components/cityList';

export default {
  name:'City',
  components:{
    CityHeader:CityHeader,
    CityList
  }
}
</script>

<style>

</style>
