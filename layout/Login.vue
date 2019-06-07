<template>
  <view class="container">
    <slot/>
  </view>
</template>

<script>
export default {};
</script>

<style>
.container {
  position: relative;
  width: 100%;
  height: 100%;
  padding: 30px;
  background-color: #f1f3f5;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
