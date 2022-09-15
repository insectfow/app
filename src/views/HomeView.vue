<template>
  <div class="home">
    <image-resize-vue />
    <image-resize-vue2 />
  </div>
</template>

<script>
import ImageResizeVue from "@/components/ImageResize.vue";
import ImageResizeVue2 from "@/components/ImageResize2.vue";
export default {
  name: "HomeView",
  data() {
    return {};
  },
  components: {
    ImageResizeVue,
    ImageResizeVue2,
  },
  methods: {},
};
</script>
<style></style>
