<template>
  <app-navigation class="page"></app-navigation>
</template>

 <script>
import { StackNavigator } from "vue-native-router";
import Main from "./page/main/Main.vue";
import Test from "./page/main/Test.vue";
const AppNavigation = StackNavigator(
  {
    Main: {
      screen: Main,

      navigationOptions: navigation => {
        //   console.log(navigation);
        return {
          title: "10",
          header: null
        };
      }
    },
    Test: Test
  },
  {
    initialRouteName: "Main",
    contentOptions: {
      activeTintColor: "#e91e63"
    },
    contentComponent: props => {
      // console.log("props inside contentComponent", props);
      return <SideBarScreen {...props} />;
    }
  }
);
export default {
  components: {
    AppNavigation
  },
  methods: {
    movePage(name) {
      //AppNavigation.navigate(name);
    },
    onPressLearnMore() {
      // console.log(AppNavigation);
      // AppNavigation.n
      avigate("Test");
    }
  }
};
</script>

<style lang="scss">
.page {
  width: 100%;
}
.container {
  background-color: #f5f5f5;
  align-items: center;
  justify-content: center;
  flex: 1;
}
</style>
