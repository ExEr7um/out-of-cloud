<template>
  <div class="home">
    <div class="slider-container">
      <h2>Взгляните на процесс сборки своими глазами</h2>
      <Slider />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Slider from "@/components/Slider.vue";

export default {
  name: "Home",
  components: {
    Slider,
  },
};
</script>

<style lang="scss" scoped>
.slider-container {
  display: flex;
  flex-direction: column;
  align-items: center;

  h2 {
    margin-bottom: 29px;
  }
}
</style>
