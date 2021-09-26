<template>
  <agile :options="options">
    <img
      :class="`img-fluid ${customStyle}`"
      :src="image"
      v-for="(image, index) in images"
      :key="index"
    />
  </agile>
</template>

<script>
import { VueAgile } from "vue-agile";
export default {
  name: "ImageSlider",
  props: ["images", "customStyle"],
  components: {
    agile: VueAgile,
  },
  data() {
    return {
      options: {
        autoplay: true,
        autoplaySpeed: 5000,
        dots: false,
        fade: true,
        navButtons: false,
      },
    };
  },
};
</script>