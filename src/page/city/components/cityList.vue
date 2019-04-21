<template>
  <div class="list" ref="wrapper">
    <!-- 这个无类名DIV结合于better-scroll的文件结构 -->
      <div>
          <!-- 当前城市 -->
        <div class="item ">
          <div class="item-title" >当前城市</div>
          <div class="item-city">
            <div class="city">{{this.$store.state.city}}</div>
          </div>
        </div>
        <!-- 热门城市 -->
        <div class="item ">
          <div class="item-title">热门城市</div>
            <div class="item-city" v-for='item of listDatas' :key="item.id" @click="handleClick(item.name)">
              <div class="city">{{item.name}}</div>            
            </div>
        </div>
        
        <!-- 字母城市 -->
        <div class="item" v-for="(value,key,index) of alphabetDatas" :key="index" :ref="key">
          <div class="item-title" @click="handleClick">{{key}}</div>
          <div class="item-str" v-for='item of value' :key="item.id" @click="handleClick(item.name)" >
            <div class="str">{{item.name}}</div>
          </div>
      
        </div>
      </div>
    

  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name:'CityList',
  props:{
    listDatas:Array,
    alphabetDatas:Object,
    letters:String,
  },
  methods:{
    handleClick(city){
      this.$store.dispatch('changeCity',city)
      this.$router.push('/')
    }
  },
  watch:{
    letters(){
      if(this.letters.length){
        const element = this.$refs[this.letters][0]
        console.log(element)
        this.myscroll.scrollToElement(element)
      }
    }
  },
  mounted(){
    this.myscroll = new BScroll(this.$refs.wrapper,{
      click:true
    })
  }
};
</script>

<style lang='stylus' scoped>
@import '~@/assets/styles/varibles.styl'
.list
  overflow hidden
  position absolute
  top:1.68rem
  left 0
  right 0
  bottom 0
  .item
    overflow auto
   
    .item-title
      background #eee
      height 0.68rem
      line-height 0.68rem
      padding-left 0.15rem
      border-color #ccc
    .item-city
      width 33.33%
      float left
      overflow hidden
      .city
        text-align center
        border 0.02rem solid #ccc
        padding 0.1rem 0
        border-radius 0.06rem
        margin 0.1rem
        border-color #ccc
    .item-str
      .str
        padding 0.1rem
        border-bottom 0.01rem solid #ccc
        line-height 0.58rem
        border-color #ccc



  .border
    &:before
      border-color #ccc
    &:after
      border-color #ccc
  
</style>
