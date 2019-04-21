<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont balckicon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont inputicon">&#xe632;</span>
      测试后续会跳转搜索页
    </div>
    <router-link to="/city">
      <div class="header-right">
        <div class="cityname">
            {{this.$store.state.city}}
        </div>
        <span class="iconfont downicon">&#xe62d;</span>
      </div>
      
    </router-link>  
  </div>
</template>

<script>
export default {
  name: "HomeHeader"
};
</script>
<style lang='stylus' scoped>
// @import '../../../assets/styles/varibles.styl'
  @import '~@/assets/styles/varibles.styl'
.header {
  display: flex;
  height: 0.86rem;
  line-height: 0.86rem;
  background: $bgColor;
  color: #fff;
  align-items: center;

  .header-left {
    width: 0.64rem;
    float: left;

    .balckicon {
      text-align: center;
      font-size: 0.4rem;
    }
  }

  .header-input {
    flex: 1;
    height: 0.64rem;
    line-height: 0.64rem;
    background: #fff;
    border-radius: 0.1rem;
    color: #ccc;
    padding-left: 0.2rem;
  }

  .header-right {
    min-width: 1.24rem;
    padding: 0.1rem
    float: right;
    text-align: center;
    color: #eee;
    .cityname {
      display inline-block
    }
      
  }
  
}
</style>
