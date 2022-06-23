<template>
  <my-header></my-header>

  <main class="main">
    <home-section></home-section>
    <sponsor-section></sponsor-section>
    <specs-section></specs-section>
    <case-section></case-section>
    <discount-section></discount-section>
    <products-section></products-section>
  </main>

  <my-footer></my-footer>
</template>

<script>
import MyHeader from "@/components/MyHeader.vue";
import MyFooter from "@/components/MyFooter.vue";
import HomeSection from "@/components/Sections/HomeSection.vue";
import SponsorSection from "@/components/Sections/SponsorSection.vue";
import SpecsSection from "@/components/Sections/SpecsSection.vue";
import CaseSection from "@/components/Sections/CaseSection.vue";
import DiscountSection from "@/components/Sections/DiscountSection.vue";
import ProductsSection from "@/components/Sections/ProductsSection/ProductsSection.vue";

export default {
  name: "App",
  components: {
    MyHeader,
    MyFooter,
    HomeSection,
    SponsorSection,
    SpecsSection,
    CaseSection,
    DiscountSection,
    ProductsSection,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@100;200;300;400;500;600;700;900&display=swap");

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

:root {
  --header-height: 3rem;

  --hue-color: 206;

  --first-color: hsl(var(--hue-color), 4%, 4%);
  --first-color-alt: hsl(var(--hue-color), 4%, 8%);
  --title-color: hsl(var(--hue-color), 4%, 95%);
  --text-color: hsl(var(--hue-color), 4%, 75%);
  --text-color-ligth: hsl(var(--hue-color), 4%, 65%);
  --white-color: #fff;
  --body-color: hsl(var(--hue-color), 4%, 6%);
  --container-color: hsl(var(--hue-color), 4%, 10%);
  --text-gradient: linear-gradient(
    hsl(var(--hue-color), 4%, 24%),
    hsl(var(--hue-color), 4%, 8%)
  );
  --scroll-thumb-color: hsl(var(--hue-color), 4%, 16%);
  --scroll-thumb-color-alt: hsl(var(--hue-color), 4%, 20%);

  --body-font: "Roboto", sans-serif;

  --biggest-font-size: 5rem;
  --bigger-font-size: 3.5rem;
  --big-font-size: 2.5rem;
  --h2-font-size: 1.25rem;
  --h3-font-size: 1.125rem;
  --normal-font-size: 0.938rem;
  --small-font-size: 0.813rem;
  --smaller-font-size: 0.75rem;
  --text-line-height: 2rem;

  --font-medium: 500;
  --font-semi-bold: 600;

  --z-tooltip: 10;
  --z-fixed: 100;
}

@media screen and (min-width: 968px) {
  :root {
    --biggest-font-size: 7.5rem;
    --bigger-font-size: 4.5rem;
    --big-font-size: 4rem;
    --h2-font-size: 1.5rem;
    --h3-font-size: 1.25rem;
    --normal-font-size: 1rem;
    --small-font-size: 0.875rem;
    --smaller-font-size: 0.813rem;
  }
}

* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: var(--header-height) 0 0 0;
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
  background-color: var(--body-color);
  color: var(--text-color);
  line-height: 1.5;
}

h1,
h2,
h3,
h4 {
  color: var(--title-color);
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
}

button,
input {
  border: none;
  outline: none;
}

button {
  cursor: pointer;
}

img {
  max-width: 100%;
  height: auto;
}

.container {
  max-width: 968px;
  margin-left: 1.5rem;
  margin-right: 1.5rem;
}

.grid {
  display: grid;
}

.section {
  padding: 4rem 0 2rem;
}

.section__title {
  font-size: var(--bigger-font-size);
  text-align: center;
  margin-bottom: 2.5rem;
}

.section__title-gradient {
  background: var(--text-gradient);
  color: transparent;
  background-clip: text;
}

.header {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: var(--z-fixed);
  background: transparent;
}

.main {
  overflow: hidden;
}

::-webkit-scrollbar {
  width: 0.6rem;
  border-radius: 0.5rem;
}

::-webkit-scrollbar-thumb {
  background-color: var(--scroll-thumb-color);
  border-radius: 0.5rem;
}

::-webkit-scrollbar-thumb:hover {
  background-color: var(--scroll-thumb-color-alt);
}

.button {
  display: inline-block;
  background-color: var(--first-color);
  color: var(--white-color);
  padding: 1rem 1.25rem;
  border-radius: 0.5rem;
  transition: 0.3s;
}

.button:hover {
  background-color: var(--first-color-alt);
}

.button__icon {
  font-size: 1.2rem;
}

.button--flex {
  display: inline-flex;
  align-items: center;
  column-gap: 0.75rem;
}

@media screen and (max-width: 340px) {
  .container {
    margin-left: 1rem;
    margin-right: 1rem;
  }

  .section__title {
    font-size: var(--big-font-size);
  }
}

@media screen and (min-width: 767px) {
  body {
    margin: 0;
  }

  .section {
    padding: 6rem 0 2rem;
  }
}

@media screen and (min-width: 1024px) {
  .container {
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
