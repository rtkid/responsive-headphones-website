<template>
  <section class="case section grid" id="case">
    <h2 class="section__title section__title-gradient">Кейс</h2>

    <div class="case__container container grid">
      <div>
        <img src="@/assets/img/case.png" alt="" class="case__img" />
      </div>

      <div class="case__data">
        <p class="case__description">
          С комфортным и удобным кейсом, так что вы можите хранить их где хотите
          и сохранять свою долговечность.
        </p>

        <a href="#" class="button button--flex">
          <i class="ri-information-line button__icon"></i> Больше информации
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.case__container {
  position: relative;
  grid-template-columns: repeat(2, 1fr);
}

.case__data {
  padding: 5rem 0 3rem;
}

.case__img {
  width: 250px;
  position: absolute;
  left: -7rem;
}

.case__description {
  margin-bottom: 1.5rem;
  line-height: var(--text-line-height);
}

@media screen and (max-width: 340px) {
  .case__container {
    grid-template-columns: 0.6fr 1fr;
  }

  .case__img {
    width: 220px;
    top: -2rem;
    left: -9rem;
  }

  .case__data {
    padding: 0;
  }
}

@media screen and (min-width: 576px) {
  .case__img {
    position: initial;
  }

  .case__data {
    padding: 0;
  }

  .case__container {
    grid-template-columns: max-content 250px;
    justify-content: center;
    align-items: center;
    column-gap: 2rem;
  }
}

@media screen and (min-width: 767px) {
  .case__img {
    width: 300px;
  }

  .case__description {
    margin-bottom: 2rem;
  }
}
</style>
