<template>
  <v-container fluid class="grey darken-3 white--text">
    <v-row>
        <v-col cols="2"></v-col>
        <v-col cols="4">
          <p>Contact:</p>
          <p>Email: matepabon@gmail.com</p>
          <i class="far fa-envelope"></i>
        </v-col>
        <v-col cols="4">
          <p>Social Networks:</p>
          <a href="https://www.instagram.com/tears_spirit/?hl=es-la" target="_blank">
            <i class="fab fa-instagram"></i>
          </a>
          &nbsp;
          <a href="https://github.com/Kathar6" target="_blank">
            <i class="fab fa-github"></i>
          </a>
        </v-col>
        <v-col cols="2"></v-col>
    </v-row>
    <v-row>
        <v-col cols="12" class="text-center">
            <h4>© Kathar6 2020</h4>
        </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "app-footer"
};
</script>

<style lang="scss" scoped>
@import "../scss/_variables.scss";

a{
  background-color:transparent;
  color:unset;
  text-decoration: none;
  &:hover, &:link, &:visited{
    color:unset;
    text-decoration:none; 
  }
}
i{
  font-size:5vw;
}
</style>