<template>
  <div class="slider">
    <div class="change-slide desktop left" @click="desiredSlide -= 1">
      <img src="@/assets/icn_arrow-left.svg" alt="<" />
    </div>
    <div class="slide">
      <div class="photo">
        <img
          :src="slides[currentSlide].photo"
          :alt="slides[currentSlide].title"
        />
        <div class="number">{{ currentSlide + 1 }}</div>
      </div>
      <div class="text">
        <h4>{{ slides[currentSlide].title }}</h4>
        <p>
          {{ slides[currentSlide].description }}
        </p>
      </div>
    </div>
    <div class="change-slide desktop right" @click="desiredSlide += 1">
      <img src="@/assets/icn_arrow-left.svg" alt=">" />
    </div>
    <div class="mobile-slide-changer">
      <div class="change-slide left" @click="desiredSlide -= 1">
        <img src="@/assets/icn_arrow-left.svg" alt="<" />
      </div>
      <div class="change-slide right" @click="desiredSlide += 1">
        <img src="@/assets/icn_arrow-left.svg" alt=">" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    slides: {
      type: Array,
      default: null,
    },
  },
  data() {
    return {
      currentSlide: 0,
      desiredSlide: 0,
    };
  },
  watch: {
    desiredSlide: function () {
      if (this.desiredSlide > this.slides.length - 1) {
        this.desiredSlide = 0;
      } else if (this.desiredSlide < 0) {
        this.desiredSlide = this.slides.length - 1;
      }
      this.currentSlide = this.desiredSlide;
    },
  },
};
</script>

<style lang="scss" scoped>
.slider {
  display: flex;
  align-items: center;

  .change-slide {
    cursor: pointer;
    display: flex;

    &.desktop {
      margin: 0 30px;
    }

    &.right {
      transform: rotate(180deg);
    }
  }

  .mobile-slide-changer {
    display: none;
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

    .photo {
      width: 560px;
      height: 284px;
      background: #c4c4c4;
      position: relative;
      overflow: hidden;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }

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

@media (max-width: 950px) {
  .slider {
    flex-direction: column;
    width: 100vw;
    padding: 0 20px;

    .mobile-slide-changer {
      margin-top: 33px;
      display: flex;
      align-items: center;
      gap: 60px;
    }

    .change-slide.desktop {
      display: none;
    }

    .slide {
      height: 350px;
      width: 100%;
      max-width: 450px;
      padding: 20px;

      .photo {
        height: 160px;
        width: 100%;
      }

      .number {
        width: 40px;
        height: 40px;
        left: -8px;
        top: -9px;
      }
    }
  }
}
</style>
