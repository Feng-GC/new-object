<template>
  <div class="search">
    <input type="text" placeholder="请输入城市名" class="search-input">
  </div>
</template>

<script>
export default {
  name:'CitySearch'
}
</script>

<style lang='stylus' scoped>
@import '~@/assets/styles/varibles.styl'
  .search
    height 0.68rem
    overflow hidden
    text-align center
    background $bgColor
    padding 0.1rem
    .search-input
      width 100%
      border none
      border-radius 0.1rem 
      height 95%
</style>
