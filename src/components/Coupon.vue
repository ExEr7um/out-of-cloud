<template>
  <div class="coupon">
    <div class="icon-container">
      <img :src="icon" />
    </div>
    <div class="text">
      <h2>
        {{ title.row1 }}<br /><span>{{ title.row2 }}</span>
      </h2>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: null,
      default: null,
    },
    title: {
      type: Object,
      default: null,
    },
    description: {
      type: String,
      default: null,
    },
  },
};
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
