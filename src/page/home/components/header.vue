<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont balckicon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont inputicon">&#xe632;</span>
      main
    </div>
    <div class="header-right">
      rihgt
      <span class="iconfont downicon">&#xe62d;</span>
    </div>
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
    width: 1.24rem;
    float: right;
    text-align: center;
  }
}
</style>
