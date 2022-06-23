<template>
  <article class="card">
    <div class="card__content">
      <img :src="imgSrc" alt="" class="card__img" />
      <h3 class="card__title">{{ title }}</h3>
      <span class="card__price">{{ price }}</span>

      <button class="button button--flex card__button">
        <i class="ri-shopping-bag-line button__icon"></i>
      </button>
    </div>
  </article>
</template>

<script>
export default {
  props: {
    imgSrc: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    price: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.card {
  position: relative;
  height: 132px;
  background-color: var(--container-color);
  padding: 0.75rem;
  border-radius: 0.5rem;
  display: grid;
}

.card__img {
  width: 80px;
  position: absolute;
  inset: 0;
  margin-left: auto;
  margin-right: auto;
  top: -3rem;
}

.card__content {
  align-self: flex-end;
}

.card__title,
.card__price {
  font-size: var(--small-font-size);
}

.card__price {
  font-weight: var(--font-semi-bold);
}

.card__button {
  position: absolute;
  right: 0.5rem;
  bottom: 0.5rem;
  padding: 0.5rem;
  border-radius: 0.35rem;
}

@media screen and (min-width: 767px) {
  .card {
    height: 152px;
    padding: 0.85rem;
  }

  .card__img {
    width: 95px;
  }
}
</style>
