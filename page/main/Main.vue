<template>
  <view class="container">
    <text>Main</text>
    <view class="menu-box">
      <text class="menu">test</text>
      <text class="menu">test</text>
      <text class="menu">test</text>
      <text class="menu">test</text>
    </view>
  </view>
</template>

<script>
export default {
  propsData: {},
  data() {
    return {};
  }
};
</script>

<style lang="scss">
.container {
  width: 100%;
  height: 100%;
  padding: 30px;
  color: black;
  background-color: #333;
}
.menu-box {
  margin: 0px;
  display: flex;
  flex-direction: row;
  align-items: stretch;
  justify-content: center;
  position: absolute;
  height: 85px;
  bottom: 0px;
  left: 0px;
  right: 0px;
  background-color: #fff;
}
.menu {
  padding: 10px;
  border-left-width: 1px;
  border-left-color: rgba(0, 0, 0, 0.05);
  text-align: center;
  width: 25%;
}
</style>
