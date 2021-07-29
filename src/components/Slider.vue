<template>
  <div class="slider">
    <div class="change-slide left">
      <img src="@/assets/icn_arrow-left.svg" alt="<" />
    </div>
    <div class="slide">
      <div class="video">
        <div class="number">1</div>
      </div>
      <div class="text">
        <h4>Привезём точно по списку</h4>
        <p>
          Сборщик берëт с собой наручный терминал, на котором он видит весь
          список покупок для каждого заказа.
        </p>
      </div>
    </div>
    <div class="change-slide right">
      <img src="@/assets/icn_arrow-left.svg" alt=">" />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.slider {
  display: flex;
  align-items: center;

  .change-slide {
    margin: 0 30px;
    cursor: pointer;

    &.right {
      transform: rotate(180deg);
    }
  }

  .slide {
    width: 640px;
    height: 450px;
    background: white;
    box-shadow: 0px 0px 40px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 40px 40px 10px;

    .video {
      width: 560px;
      height: 284px;
      background: #c4c4c4;
      position: relative;

      .number {
        width: 50px;
        height: 50px;
        position: absolute;
        top: -12px;
        left: -4px;
        background: white;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 100%;
        font-size: 22px;
        color: #7db945;
        font-family: "Rotonda";
        font-weight: bold;
      }
    }

    .text {
      margin-top: 28px;
      text-align: center;
      max-width: 500px;
    }
  }
}
</style>
