<template>
  <div id="app">
    <v-toolbar app>
      <v-toolbar-side-icon>
        <img class="navbar-logo" src="./assets/wolf-logo-sm.webp" />
      </v-toolbar-side-icon>
      <v-toolbar-title>Wolf Mastering</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items
        class="hidden-sm-and-down"
        v-for="(item, i) in navBarItems"
        :key="i"
      >
        <v-btn :to="item.link" flat>{{ item.name }}</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content>
      <v-container fluid> <router-view></router-view> </v-container>
    </v-content>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      navBarItems: [
        { name: "Home", link: "/" },
        { name: "Equipment", link: "/equipment" },
        { name: "Clients", link: "/clients" },
        { name: "Samples", link: "/samples" },
        { name: "Prices", link: "/prices" },
        { name: "Contact", link: "/contact" }
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.navbar-logo {
  height: 46px;
}
</style>
