<template>
  <v-parallax dark :src="require('../assets/studio-knobs-md.jpg')">
    <v-layout align-center column justify-center>
      <h1 class="display-4 font-weight-bold mb-3 para-heading">{{ title }}</h1>
      <h4 class="title font-italic">{{ content }}</h4>
    </v-layout>
  </v-parallax>
</template>

<script>
export default {
  name: "ParallaxHeader",
  props: { title: String, content: String }
};
</script>

<style></style>
