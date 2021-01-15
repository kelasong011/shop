<template>
  <footer class="footer_guide">
    <span class="guide_item" :class="{on:iscurrent('/msite')}" @click="goto('/msite')">
      <span>
        <i class="iconfont icon-waimai"></i>
      </span>
      <span>外卖</span>
    </span>
    <span class="guide_item" :class="{on:iscurrent('/search')}" @click="goto('/search')">
      <span>
        <i class="iconfont icon-search"></i>
      </span>
      <span>搜索</span>
    </span>
    <span class="guide_item" :class="{on:iscurrent('/order')}"  @click="goto('/order')">
      <span>
        <i class="iconfont icon-dingdan"></i>
      </span>
      <span>订单</span>
    </span>
    <span class="guide_item" :class="{on:iscurrent('/profile')}"  @click="goto('/profile')">
      <span>
        <i class="iconfont icon-geren"></i>
      </span>
      <span>我的</span>
    </span>
  </footer>
</template>

<script>
export default {
  methods:{
    iscurrent(path){
      return this.$route.path === path
    },
    //点击跳转对应路由
    goto(path){
     this.$router.replace(path)
    }
  }
};
</script>

<style lang='stylus' rel="stylesheet/stylus">
@import "../../common/stylus/mixins.styl"
.footer_guide
  top-border-1px(#cccccc)
  z-index 100
  display flex
  position fixed
  left 0
  bottom 0
  width 100%
  height 50px
  background-color #fff
  .guide_item
    display flex
    flex-direction column
    text-align center
    width 25%
    &.on
      color red
    span
      margin-top 4px
      font-size 12px
      .iconfont
        font-size 22px
</style>