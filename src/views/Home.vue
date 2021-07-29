<template>
  <div class="home">
    <div class="slider-container">
      <h2>Взгляните на процесс сборки своими глазами</h2>
      <Slider />
    </div>
    <div class="coupons-container">
      <div class="coupons">
        <Coupon />
        <h2 class="plus">+</h2>
        <Coupon />
      </div>
      <button class="main open-popup">К покупкам</button>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Slider from "@/components/Slider.vue";
import Coupon from "@/components/Coupon.vue";

export default {
  name: "Home",
  components: {
    Slider,
    Coupon,
  },
};
</script>

<style lang="scss" scoped>
.slider-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 80px;

  h2 {
    text-align: center;
    margin-bottom: 29px;
  }
}

.coupons-container {
  background: white;
  padding: 60px 0 100px;
  display: flex;
  align-items: center;
  flex-direction: column;

  .coupons {
    display: flex;
    align-items: center;
    margin-bottom: 50px;

    .plus {
      margin: 0 40px;
    }
  }

  .open-popup {
    width: 340px;
  }
}
</style>
