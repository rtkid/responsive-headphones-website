<template>
  <section class="discount section">
    <div class="discount__container container grid">
      <div class="discount__animate">
        <h2 class="discount__title">
          Погрузитесь в
          <br />
          музыку
        </h2>

        <p class="discount__description">Получи это сейчас, скидка до 50%.</p>

        <a href="#" class="button button--flex">
          <i class="ri-shopping-bag-line button__icon"></i> Купить Сейчас
        </a>
      </div>

      <img src="@/assets/img/discount.png" alt="" class="discount__img" />
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.discount__container {
  position: relative;
  background-color: var(--container-color);
  padding: 2rem 1.5rem;
  border-radius: 0.75rem;
}

.discount__title {
  font-size: var(--h3-font-size);
  margin-bottom: 0.75rem;
}

.discount__description {
  margin-bottom: 1rem;
}

.discount__img {
  width: 300px;
  position: absolute;
  top: 4rem;
  right: -11rem;
}

@media screen and (min-width: 576px) {
  .discount__img {
    position: initial;
  }

  .discount__container {
    grid-template-columns: repeat(2, 1fr);
    justify-items: center;
    align-items: center;
  }
}

@media screen and (min-width: 767px) {
  .discount__container {
    grid-template-columns: 250px max-content;
    justify-content: center;
    column-gap: 5rem;
    padding: 3rem 0;
  }

  .discount__title {
    font-size: var(--h2-font-size);
    margin-bottom: 1rem;
  }

  .discount__description {
    margin-bottom: 2rem;
  }
}

@media screen and (min-width: 1024px) {
  .discount__img {
    width: 350px;
  }
}
</style>
