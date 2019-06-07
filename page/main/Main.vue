<template>
  <login-layout>
    <text class="top-circle"></text>
    <text class="small-circle circle1"></text>
    <text class="small-circle circle2"></text>
    <text class="small-circle circle3"></text>
    <text class="bottom-circle"></text>
    <text class="gradient"></text>
    <view class="content">
      <text class="cb fs2 ta-c">LOGIN PAGE</text>
      <text-input
        class="input input-id"
        :on-focus="onFocus(true)"
        :on-blur="onFocus(false)"
        v-model="form.id"
      />
      <text-input
        class="input input-password"
        :on-focus="onFocus(true)"
        :on-blur="onFocus(false)"
        v-model="form.password"
      />
      <touchable-opacity :on-press="onPressButton" class="login-btn" :class="focus">
        <text class="button-text">LOGIN</text>
      </touchable-opacity>
    </view>
  </login-layout>
</template>

<script>
import LoginLayout from "../../layout/Login.vue";

export default {
  components: {
    LoginLayout
  },
  data() {
    return {
      form: {
        id: "",
        password: ""
      },
      focus: false
    };
  },
  methods: {
    onPressButton() {},
    onFocus(type) {
      this.focus = type;
    }
  }
};
</script>

<style lang="scss">
@import "../../style/text.scss";
.focus {
  border-color: salmon;
}
.top-circle {
  background-color: #f783ac;
  width: 1280px;
  height: 1280px;
  border-radius: 640px;
  position: absolute;
  top: -143%;
  left: -70%;
  elevation: 20;
}
.small-circle {
  background-color: #faa2c1;
  width: 100px;
  height: 100px;
  border-radius: 50px;
  position: absolute;
  elevation: 10;
}
.circle1 {
  left: 7%;
  top: 13%;
}
.circle2 {
  width: 75px;
  height: 75px;
  border-radius: 50px;
  left: 90%;
  top: 31%;
}
.circle3 {
  background-color: #fcc2d7;
  width: 75px;
  height: 75px;
  border-radius: 50px;
  left: 70%;
  top: 85%;
}
.bottom-circle {
  opacity: 0.9;
  background-color: #f783ac;
  width: 500px;
  height: 500px;
  border-radius: 250px;
  position: absolute;
  bottom: -35%;
  left: -76%;
  elevation: 10;
}
.gradient {
  position: absolute;
  background-color: rgba(255, 255, 255, 0.5);
  top: 0px;
  left: 0px;
  right: 0px;
  bottom: 0px;
}

.content {
  z-index: 10;
  width: 80%;
}
.ta-c {
  text-align: center;
}
.cp {
  color: #f06595;
}
.cb {
  color: #343a40;
}
.fs2 {
  font-size: 32px;
}
.input {
  margin-top: 32px;
  font-size: 16px;
  padding: 16px;
  border-color: rgba(0, 0, 0, 0.15);
  border-width: 1px;
  border-radius: 10px;
}
.input-password {
  margin-top: 16px;
}

.login-btn {
  width: 100%;
  background-color: #f06595;
  border-radius: 10px;
  margin-top: 32px;
  padding: 16px;
  font-size: 16px;
}
.button-text {
  text-align: center;
  color: #fff;
  font-size: 16px;
}
</style>
