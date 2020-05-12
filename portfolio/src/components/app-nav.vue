<template>
  <div>
        <v-app-bar
        color="grey darken-4"
        dense
        dark
        >
        <v-app-bar-nav-icon></v-app-bar-nav-icon>

        <v-toolbar-title>Portfolio</v-toolbar-title>

        <v-spacer></v-spacer>
        </v-app-bar>
  </div>
</template>

<script>
export default {
    name: "app-nav"
}
</script>

<style lang="scss" scoped>
    // @import "../scss/_variables.scss";
    // /* # Header Styles */
    // .nav{
    //     display:grid;
    //     grid-template-columns:1fr 1fr 1fr 1fr 1fr;
    //     width:100vw;
    //     height:10vh;
    //     max-height: 12vh;
    //     padding:0;
    //     margin:0;
    //     background-color:$black;
    //     color:white;
    //     h3{
    //         grid-column:3/4;
    //         padding:5% 10%;
    //     }
    // }
</style>