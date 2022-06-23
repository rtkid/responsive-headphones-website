<template>
  <section class="sponsor section">
    <div class="sponsor__container container grid">
      <img
        v-for="img in sponsorImages"
        :key="img.src"
        :src="img.src"
        alt=""
        class="sponsor__img"
      />
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      sponsorImages: [
        { src: require("@/assets/img/sponsor1.png") },
        { src: require("@/assets/img/sponsor2.png") },
        { src: require("@/assets/img/sponsor3.png") },
        { src: require("@/assets/img/sponsor4.png") },
      ],
    };
  },
};
</script>

<style scoped>
.sponsor__img {
  width: 90px;
}

.sponsor__container {
  grid-template-columns: repeat(auto-fit, minmax(110px, 1fr));
  row-gap: 5rem;
  justify-items: center;
  align-items: center;
}

@media screen and (min-width: 1024px) {
  .sponsor__img {
    width: 100px;
  }
}
</style>
