<template>
  <div class="list">
    <div class="item">A</div>
    <div class="item">B</div>
    <div class="item">C</div>
    <div class="item">D</div>
    <div class="item">E</div>
  </div>
</template>

<script>
export default {
  name:'CityAlphabet'
}
</script>

<style lang='stylus' scoped>
  .list
    position absolute
    top 2.70rem
    right 0.05rem
    display flex
    flex-direction column
    justify-content  center
    overflow hidden
    .item
      height 0.5rem
      width 0.5rem
      font-size 0.25rem
      font-weight bold 
      text-align center
    
      
     
</style>
