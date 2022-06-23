<template>
  <section class="home section" id="home">
    <div class="home__container container grid">
      <div>
        <img src="@/assets/img/home.png" alt="" class="home__img" />
      </div>

      <div class="home__data">
        <div class="home__header">
          <h1 class="home__title">Наушники</h1>
          <h2 class="home__subtitle">Beats 3</h2>
        </div>

        <div class="home__footer">
          <h3 class="home__title-description">Обзор</h3>
          <p class="home__description">
            Наслаждайтесь отмеченный наградами Beats звук с обтекаемым дизайном
            и удобными мягкими наушниками, обеспечивающие первоклассное
            звучание.
          </p>
          <a href="#" class="button button--flex">
            <span class="button--flex">
              <i class="ri-shopping-bag-line button__icon"></i>
              Добавить в Корзину
            </span>
            <span class="home__price">$299</span>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.home__img {
  width: 250px;
  position: absolute;
  top: -16rem;
  right: 1.5rem;
}

.home__data {
  padding-top: 5rem;
}

.home__header {
  position: relative;
}

.home__title {
  font-size: var(--biggest-font-size);
  background: var(--text-gradient);
  color: transparent;
  background-clip: text;
  position: absolute;
  top: -4rem;
  left: 1rem;
  line-height: 6rem;
}

.home__subtitle {
  font-size: var(--big-font-size);
  margin-bottom: 2.5rem;
}

.home__title-description {
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  margin-bottom: 1rem;
}

.home__description {
  margin-bottom: 2.5rem;
  line-height: 2rem;
}

.home__price {
  font-size: var(--h3-font-size);
  font-weight: var(--font-semi-bold);
  margin-left: 0.75rem;
}

@media screen and (max-width: 340px) {
  .home__img {
    width: 200px;
    top: -13rem;
  }

  .home__title {
    top: -4rem;
    font-size: 3rem;
  }

  .home__data {
    padding-top: 1rem;
  }

  .home__description {
    font-size: var(--small-font-size);
  }
}

@media screen and (min-width: 576px) {
  .home__container {
    grid-template-columns: 0.8fr 1fr;
  }

  .home__data {
    padding-top: 2rem;
  }

  .home__img {
    top: -7rem;
    left: 0;
  }
}

@media screen and (min-width: 767px) {
  .home__container {
    position: relative;
    grid-template-columns: repeat(2, 1fr);
  }

  .home__img {
    top: -9rem;
    left: 4rem;
  }

  .home__data {
    padding-top: 8rem;
  }
}

@media screen and (min-width: 1024px) {
  .home__img {
    width: 300px;
    top: -15rem;
  }

  .home__title {
    top: -5rem;
    left: 3.5rem;
  }

  .home__description {
    padding-right: 5rem;
  }
}
</style>
