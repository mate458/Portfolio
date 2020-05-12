<template>
  <v-app id="app">
    <app-nav />
    <app-body2 />
    <app-footer />
  </v-app>
</template>

<script>
import AppNav from "./components/app-nav";
import AppBody2 from "./components/app-body2";
import AppFooter from "./components/app-footer";
export default {
  name: "App",

  components: {
    AppNav,
    AppBody2,
    AppFooter
  },

  data: () => ({
    //
  })
};
</script>


<style lang="scss">
@font-face {
  font-family: "OpenSans";
  src: url("../public/Fonts/OpenSans-Regular.ttf");
}
* {
  font-family: "OpenSans", Arial, Helvetica, sans-serif;
}
body {
  overflow: hidden;
}
a, i{
  cursor: pointer;
}
hr {
  margin: 2vh 3vw 0vh 3vw;
}
#app {
  background-image: url("../public/Img/background_portfolio.jpg");
  background-size: cover;
  background-attachment: fixed;
  transition:all .7s;
}
</style>