<template>
  <section class="products section" id="products">
    <h2 class="section__title section__title-gradient products__line">
      Выбери
      <br />
      Свой Стиль
    </h2>

    <div class="products__container container grid">
      <product-card
        v-for="card in cards"
        :key="card.title"
        :imgSrc="card.imgSrc"
        :title="card.title"
        :price="card.price"
      ></product-card>
    </div>
  </section>
</template>

<script>
import ProductCard from "@/components/Sections/ProductsSection/ProductCard.vue";

export default {
  components: {
    ProductCard,
  },

  data() {
    return {
      cards: [
        {
          imgSrc: require("@/assets/img/product1.png"),
          title: "Чёрные",
          price: "$249",
        },
        {
          imgSrc: require("@/assets/img/product2.png"),
          title: "Красно Чёрные",
          price: "$249",
        },
        {
          imgSrc: require("@/assets/img/product3.png"),
          title: "Тёмно Чёрные",
          price: "$249",
        },
        {
          imgSrc: require("@/assets/img/product4.png"),
          title: "Голубые",
          price: "$249",
        },
        {
          imgSrc: require("@/assets/img/product5.png"),
          title: "Серые",
          price: "$249",
        },
      ],
    };
  },
};
</script>

<style scoped>
.products__line {
  line-height: 4rem;
}

.products__container {
  grid-template-columns: repeat(2, 1fr);
  gap: 5rem 1.5rem;
  padding-top: 3rem;
}

@media screen and (max-width: 340px) {
  .products__container {
    grid-template-columns: 142px;
    justify-content: center;
  }
}

@media screen and (min-width: 576px) {
  .products__container {
    grid-template-columns: repeat(3, 142px);
    justify-content: center;
  }
}

@media screen and (min-width: 767px) {
  .products__container {
    grid-template-columns: repeat(3, 162px);
    gap: 6rem 3rem;
    padding-top: 5rem;
  }
}
</style>
