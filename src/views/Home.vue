<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/wolf-logo.webp" />
    <HelloWorld msg="Wolf Mastering" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>
