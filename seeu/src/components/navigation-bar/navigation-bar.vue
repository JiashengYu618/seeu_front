<template>
  <div class="navigation">
    <div class="nav-box">
      <span>
        <i class="iconfont icon-caidan06"></i>
      </span>
      <span>Home</span>
    </div>
    <div class="nav-box">
      <span>
        <i class="iconfont icon-search"></i>
      </span>
      <span>Search</span>
    </div>
    <div class="nav-box">+</div>
    <div class="nav-box">
      <span>
        <i class="iconfont icon-message1"></i>
      </span>
      <span>Inbox</span>
    </div>
    <div class="nav-box">
      <!--<span> 用于对文档中的行内元素进行组合。-->
      <!--这里从Ali加入me的图片（here add Ali 'Me Photo'）-->
      <span>
        <i class="iconfont icon-me"></i>
      </span>
      <span>Me</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "navigation-bar",
  data() {
    return {};
  }
};
</script>
<style lang='stylus' scoped>
.navigation {
  z-index: 100;
  opacity: 0.6;
  position: fixed;
  bottom: 0;
  left: 0;
  height: 45px;
  line-height: 18px; // 调节图片与文字之间的距离
  //background-color: #000000;
  width: 100%;
  border-top: 3px solid #F0F8FF; // 上边框样式border-top style
  display: flex;
  font-size: 13px;

  .nav-box {
    flex-grow: 1;
    text-align: center;
    font-size: 13px;
    color: #ffffff;
    display: flex;
    flex-direction: column;
    justify-content: center;
    justify-items: center;
  }
}
</style>