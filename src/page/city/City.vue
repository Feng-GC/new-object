<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list></city-list>
    <city-alphabet></city-alphabet>
  </div>
</template>

<script>
import CityHeader from './components/cityHeader'
import CityList from './components/cityList';
import CitySearch from './components/citySearch';
import CityAlphabet from './components/cityalphabet'

export default {
  name:'City',
  components:{
    CityHeader:CityHeader,
    CityList,
    CitySearch,
    CityAlphabet
  }
}
</script>

<style>

</style>
