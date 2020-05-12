<template>
  <div>
    <v-app-bar color="grey darken-4" fixed dense dark inverted-scroll>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Portfolio</v-toolbar-title>

      <v-spacer></v-spacer>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" fixed bottom temporary>
      <v-list nav dense>
        <v-list-item-group v-model="group" active-class="black--text text--grey-4">
          <a href="#languages">
            <v-list-item>
                <v-list-item-title>Programming Languages</v-list-item-title>
            </v-list-item>
          </a>
          <a href="#projects">
            <v-list-item>
                <v-list-item-title>Projects</v-list-item-title>
            </v-list-item>
          </a>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: "app-nav",
  data() {
    return {
      drawer: null,
      items: [{ title: "Home" }, { title: "About" }]
    };
  }
};
</script>

<style lang="scss" scoped>

/* # Header Styles */
a, a:link, a:visited{
  color:unset;
  text-decoration:none;
}
</style>