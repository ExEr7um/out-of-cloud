<template>
  <div class="home">
    <div class="slider-container">
      <h2>Взгляните на процесс сборки своими глазами</h2>
      <Slider :slides="slides" />
    </div>
    <div class="coupons-container">
      <div class="coupons">
        <Coupon
          :icon="require('@/assets/icn_discount.svg')"
          :title="{ row1: 'Скидка', row2: '1500 ₽' }"
          description="-500 ₽ на первые три заказа по промокоду NEW"
        />
        <h2 class="plus">+</h2>
        <Coupon
          :icon="require('@/assets/icn_truck.svg')"
          :title="{ row1: 'Бесплатная', row2: 'доставка' }"
          description="первого заказа"
        />
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
  data() {
    return {
      slides: [
        {
          title: "Привезём точно по списку",
          description:
            "Сборщик берëт с собой наручный терминал, на котором он видит весь список покупок для каждого заказа.",
          photo: require("@/assets/photos/photo_slide-1.png"),
        },
        {
          title: "Собираем быстро и эффективно",
          description:
            "Для улучшения эргономики пространства товары размещены от тяжëлых к лëгким, находящимся уже в конечной зоне упаковки.",
          photo: require("@/assets/photos/photo_slide-2.png"),
        },
        {
          title: "За свежесть и качество отвечаем",
          description:
            "Выделены специальные зоны, в том числе холодная и морозильная.",
          photo: require("@/assets/photos/photo_slide-3.png"),
        },
        {
          title: "Шампунь не положат рядом с рыбой",
          description:
            "Собираем и упаковываем ваш заказ с заботой: соблюдаем принципы товарного соседства и учитываем вес товара.",
          photo: require("@/assets/photos/photo_slide-4.png"),
        },
        {
          title: "Довезëм в сохранности даже яйца",
          description:
            "Бережно транспортируем контейнеры, фиксируя их стяжными ремнями. Системы охлаждения поддерживают температурный режим.",
          photo: require("@/assets/photos/photo_slide-5.png"),
        },
      ],
    };
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
