<template>
  <section class="specs section" id="specs">
    <h2 class="section__title section__title-gradient">Характеристики</h2>

    <div class="specs__container container grid">
      <div class="specs__content grid">
        <div v-for="data in specsData" :key="data.title" class="specs__data">
          <i class="specs__icon" :class="data.iconClass"></i>
          <h3 class="specs__title">{{ data.title }}</h3>
          <span class="specs__subtitle">{{ data.subtitle }}</span>
        </div>
      </div>

      <div>
        <img src="@/assets/img/specs.png" alt="" class="specs__img" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      specsData: [
        {
          title: "Соединение",
          subtitle: "Bluetooth v5.2",
          iconClass: "ri-bluetooth-line",
        },
        {
          title: "Баттарея",
          subtitle: "Длительность 40 часов",
          iconClass: "ri-battery-charge-line",
        },
        {
          title: "Зарядка",
          subtitle: "Быстрая зарядка 4.2-AAC",
          iconClass: "ri-plug-line",
        },
        {
          title: "Микрофон",
          subtitle: "Поддержка Apple Siri and Google",
          iconClass: "ri-mic-line",
        },
      ],
    };
  },
};
</script>

<style scoped>
.specs__container {
  position: relative;
}

.specs__content {
  row-gap: 1.5rem;
}

.specs__data {
  display: grid;
  row-gap: 0.25rem;
}

.specs__icon {
  font-size: 1.2rem;
  color: var(--white-color);
}

.specs__title {
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.specs__subtitle {
  font-size: var(--smaller-font-size);
}

.specs__data:nth-child(1),
.specs__data:nth-child(4) {
  margin-left: 1.5rem;
}

.specs__img {
  width: 250px;
  position: absolute;
  top: 2rem;
  right: -4rem;
}

@media screen and (max-width: 340px) {
  .specs__img {
    width: 200px;
  }
}

@media screen and (min-width: 576px) {
  .specs__img {
    position: initial;
  }

  .specs__container {
    grid-template-columns: repeat(2, 1fr);
    justify-items: center;
    align-items: center;
  }
}

@media screen and (min-width: 767px) {
  .specs__img {
    width: 300px;
  }

  .specs__container {
    column-gap: 5rem;
  }
}
</style>
