<template>
  <div class="coupon">
    <div class="icon-container">
      <img src="@/assets/icn_discount.svg" />
    </div>
    <div class="text">
      <h2>Скидка<br /><span>1500 ₽</span></h2>
      <p>-500 ₽ на первые три заказа по промокоду NEW</p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.coupon {
  border: 1px solid #d0d4cd;
  width: 390px;
  height: 217px;
  display: flex;
  padding: 30px 10px 24px 30px;

  .icon-container {
    width: 70px;
    height: 70px;
    background: #7db945;
    border-radius: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .text {
    margin-left: 30px;

    h2 {
      margin: 11px 0;

      span {
        color: #7db945;
      }
    }

    p {
      width: 250px;
    }
  }
}
</style>
