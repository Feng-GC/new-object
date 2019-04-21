<template>
 <div>
    <div class="search">
    <input type="text" placeholder="请输入城市名" class="search-input" v-model="keyWorld">
    </div>
   <div class="search-content" v-show="keyWorld" ref="citylist">
     <div>
        <div class="cols" v-for='item of list' :key="item.id" @click="handleClick(item.name)">{{item.name}}</div>
        <div class="cols" v-show="!list.length">没有找到相关信息</div>
     </div>
   </div>
 </div>  
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name:'CitySearch',
  props:{
    city:Object
  },
  data(){
    return{
      keyWorld:'',
      list:[],
      show:false,
      timer:null
    }
  },
  methods:{
    handleClick(city){
      console.log(city)
      this.$store.dispatch('changeCity',city)
      this.$router.push('/') //编程式跳转
    }
  },
  watch:{
     keyWorld(){
       this.show=true
       if(this.timer){
         clearTimeout(this.timer)
       }
       if(!this.keyWorld){
         this.list = []
         return
       }
       this.timer = setTimeout(()=>{
         const arr = []
         for(let i in this.city){
           var that = this
           this.city[i].forEach(function(item){
             if(item.name.indexOf(that.keyWorld) >-1 || item.spell.indexOf(that.keyWorld) >-1 ){
               arr.push(item)
             }
           });
         }
         console.log(arr)
         this.list = arr
       },100)
    }
  },
  mounted(){
    this.myscroll = new BScroll(this.$refs.citylist,{click:true})
  }
  
}
</script>

<style lang='stylus' scoped>
@import '~@/assets/styles/varibles.styl'
  .search
    height 0.68rem
    text-align center
    background $bgColor
    padding 0.1rem
    position relative
    .search-input
      width 100%
      border none
      border-radius 0.1rem 
      height 0.65rem
      text-align center
  .search-content
    overflow hidden
    width 100%
    z-index 1
    background #fff
    position absolute
    top  1.7rem
    left 0
    right 0
    bottom 0
    .cols
      padding 0.1rem
      border-bottom 0.01rem solid #ccc
      line-height 0.58rem 
</style>
