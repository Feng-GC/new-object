<div class="item-city">
        <div class="city">北京</div>
      </div><template>
  <div class="list">
     <!-- 当前城市 -->
    <div class="item border">
      <div class="item-title">当前城市</div>
      <div class="item-city">
        <div class="city">北京</div>
      </div>
    </div>
    <!-- 热门城市 -->
    <div class="item border">
      <div class="item-title">热门城市</div>
      <div class="item-city">
        <div class="city">北京</div>
      </div>
      <div class="item-city">
        <div class="city">北京</div>
      </div>
      <div class="item-city">
        <div class="city">北京</div>
      </div>
      <div class="item-city">
        <div class="city">北京</div>
      </div>
      <div class="item-city">
        <div class="city">北京</div>
      </div>
      <div class="item-city">
        <div class="city">北京</div>
      </div>

       
    
    </div>
    
     <!-- 字母城市 -->
    <div class="item border">
      <div class="item-title">A</div>
      <div class="item-str">
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
        <div class="str">阿尔法</div>
      </div>
    
    </div>
    

  </div>
</template>

<script>
export default {
  name:'CityList'
};
</script>

<style lang='stylus' scoped>
@import '~@/assets/styles/varibles.styl'
.list
  overflow hidden
  position absolute
  top:0.84rem
  left 0
  right 0
  bottom 0
  .item
    overflow hidden
    .item-title
      background #eee
      height 0.68rem
      line-height 0.68rem
      padding-left 0.15rem
    .item-city
      width 33.33%
      float left
      .city
        text-align center
        border 0.02rem solid #ccc
        padding 0.1rem 0
        border-radius 0.06rem
        margin 0.1rem
    .item-str
      .str
        padding 0.1rem
        border-bottom 0.01rem solid #ccc
        line-height 0.58rem



  .border
    &:before
      border-color #ccc
    &:after
      border-color #ccc
  
</style>
