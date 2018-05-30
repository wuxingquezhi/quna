<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont icon-fanhui fanhui-icon"></span>
    </div>
    <div class="header-input">
      <span class="iconfont icon-sousuo"></span>
      内容
    </div>
    <div class="header-right">
      城市<span class="iconfont icon-jiantou arrow-icon"></span>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {};
    },
    components: {}
};
</script>

<style scoped>
.header {
    line-height: 0.86rem;
    display: flex;
    background-color: #00bcdc;
    color: #fff;
}
.header-left {
    flex-basis: 0.64rem;
}
.header-input {
    color: #ccc;
    flex: 1;
    height: 0.60rem;
    line-height: 0.60rem;
    margin-top: 0.13rem;
    margin-left: 0.2rem;
    background: #fff;
    border-radius: 0.1rem;
    padding-left: .2rem;
}
.header-right {
    flex-basis: 1.60rem;
    text-align: center;
}
.arrow-icon{
    font-size: .24rem;
}
.fanhui-icon{
    text-align: center;
    font-size: .4rem;
    display: block;
    font-weight: 600;
}
</style>
