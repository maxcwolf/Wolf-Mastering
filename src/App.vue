<template>
  <div id="app">
    <v-toolbar app class="transparent elevation-0 white--text">
      <v-toolbar-side-icon v-if="navIsWhite">
        <img class="navbar-logo" src="./assets/wolf-logo-sm-white.webp" />
      </v-toolbar-side-icon>
      <v-toolbar-side-icon v-if="!navIsWhite">
        <img class="navbar-logo" src="./assets/wolf-logo-sm.webp" />
      </v-toolbar-side-icon>
      <v-toolbar-title>Wolf Mastering</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items
        class="hidden-sm-and-down"
        v-for="(item, i) in navBarItems"
        :key="i"
      >
        <v-btn :class="navIsWhite ? 'white--text' : ''" :to="item.link" flat>{{
          item.name
        }}</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content style="padding: 0;">
      <v-container fluid pa-0> <router-view></router-view> </v-container>
    </v-content>
  </div>
</template>

<script>
let resizeTimeout;
function resizeThrottler(actualResizeHandler) {
  // ignore resize events as long as an actualResizeHandler execution is in the queue
  if (!resizeTimeout) {
    resizeTimeout = setTimeout(() => {
      resizeTimeout = null;
      actualResizeHandler();

      // The actualResizeHandler will execute at a rate of 15fps
    }, 66);
  }
}

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
      ],
      colorOnScroll: 250,
      navIsWhite: true
    };
  },
  //TODO: Change handleScroll to a computed property which outputs true of false and use v-bind:class
  // to dynamically create the classes in a ternary statement.
  methods: {
    handleScroll() {
      let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
      let navbarColor = document.getElementsByClassName("v-toolbar");
      this.currentScrollValue = scrollValue;
      if (this.colorOnScroll > 0 && scrollValue > this.colorOnScroll) {
        navbarColor[0].classList.remove("transparent", "white--text");
        this.navIsWhite = false;
      } else {
        navbarColor[0].classList.add("transparent", "white--text");
        this.navIsWhite = true;
      }
    },
    scrollListener() {
      resizeThrottler(this.handleScroll);
    }
  },
  mounted() {
    document.addEventListener("scroll", this.scrollListener);
  },
  beforeDestroy() {
    document.removeEventListener("scroll", this.scrollListener);
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
