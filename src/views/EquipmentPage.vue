<template>
  <v-container fluid pa-0 grid-list-md>
    <parallax-header :title="parallaxTitle" :content="parallaxContent" />
    <v-layout fill-height row pa-4 class="main main-raised elevation-24">
      <v-flex ma-2 mt-4 xs8></v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import ParallaxHeader from "../components/ParallaxHeader";
export default {
  name: "EquipmentPage",
  components: {
    ParallaxHeader
  },
  data: () => ({
    parallaxTitle: "Equipment",
    parallaxHeader: ""
  })
};
</script>

<style></style>
