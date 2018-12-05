<template>
  <div id="app">
    <v-toolbar
      app
      class="transparent elevation-0 white--text raised-nav"
      ref="toolbar"
    >
      <v-toolbar-side-icon v-if="navIsWhite">
        <img class="navbar-logo" src="./assets/wolf-logo-sm-white.webp" />
      </v-toolbar-side-icon>
      <v-toolbar-side-icon v-if="!navIsWhite">
        <img class="navbar-logo" src="./assets/wolf-logo-sm.webp" />
      </v-toolbar-side-icon>
      <v-toolbar-title :class="{ 'white--text': navIsWhite }"
        >WOLF Mastering</v-toolbar-title
      >
      <v-spacer></v-spacer>
      <v-toolbar-items
        class="hidden-sm-and-down"
        v-for="(item, i) in navBarItems"
        :key="i"
      >
        <v-btn :class="{ 'white--text': navIsWhite }" :to="item.link" flat>{{
          item.name
        }}</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-content style="padding: 0;"> <router-view></router-view> </v-content>
  </div>
</template>

<script>
let resizeTimeout;
function resizeThrottler(resizeHandler) {
  // ignore resize events as long as an actualResizeHandler execution is in the queue
  if (!resizeTimeout) {
    resizeTimeout = setTimeout(() => {
      resizeTimeout = null;
      resizeHandler();

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
  methods: {
    handleScroll() {
      let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
      this.currentScrollValue = scrollValue;
      this.navIsWhite =
        this.colorOnScroll > 0 && scrollValue < this.colorOnScroll;
      if (!this.navIsWhite) {
        this.$refs.toolbar.$el.classList.remove("transparent", "white--text");
      } else {
        this.$refs.toolbar.$el.classList.add("transparent", "white--text");
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

.raised-nav {
  z-index: 10;
}
</style>
