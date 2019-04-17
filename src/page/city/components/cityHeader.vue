
<template>
 <div>
    <div class="head">
      <div class="head-black iconfont">&#xe624;</div>
      <div class="head-desc">城市选择</div>
    </div>

 </div>
 
</template>

<script>
export default {
  name:'CityHeader'
}
</script>

<style lang='stylus' scoped>
@import '~@/assets/styles/varibles.styl'
  .head
    width:100%
    overflow hidden
    height 0.84rem
    line-height 0.84rem
    background:$bgColor
    color:#eee 
    .head-black
      width: 0.64rem
      float left
      text-align center
    .head-desc
      text-align center
      padding 0 0.64rem
  
</style>

