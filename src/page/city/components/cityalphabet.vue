<template>
  <div>
    <div class="list" >
      <div class="item" v-for="(item,key,index) of alphabetDatas" :key="index" :ref="key"
        @click = 'handleClick'
        @touchstart= 'handletouchStart'
        @touchmove = 'handletouchMove'
        @touchend = 'handletouchEnd'
      >{{key}}</div>
  </div>
  </div>  
</template>

<script>
export default {
  name:'CityAlphabet',
  props:{
    alphabetDatas:Object
  },
  data(){
     return{
       touch:false,
       timer:null,
     }
  },
  methods:{
    handleClick:function(e){
      this.$emit('change',e.target.innerHTML)
    },
    handletouchStart(){
      this.touch = true
    },
    handletouchMove(e){
      if(this.touch){
        //console.log(e.targetTouches[0]) 触屏事件
        //$refs返回的是一个对象
        if(this.timer){
          clearTimeout(this.timer)
        }
        this.timer = setTimeout(()=>{
          const aTop = this.$refs['A'][0].offsetTop
          const touchTop = e.touches[0].clientY - 74
          const fontNum = Math.floor((touchTop - aTop)/25) 
          console.log(aTop,touchTop,fontNum+'字母')
          this.$emit('change',this.letters[fontNum])
        },5)
        
      }
    },
    handletouchEnd(){
      this.touch = false
    }, 
  },
  computed:{
    letters(){
      const letters =[]
      for(let i in this.alphabetDatas){
        letters.push(i)
      }
      return letters
    }
  }
  
}
</script>

<style lang='stylus' scoped>
    .list
      position absolute
      top 2rem
      right 0rem
      bottom 0rem
      display flex
      flex-direction column
      justify-content  center
      overflow hidden
      .item
        height 0.5rem
        width 0.5rem
        font-size 0.27rem
        text-align center

</style>
