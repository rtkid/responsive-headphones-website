<template>
  <footer class="footer section">
    <div class="footer__container container grid">
      <a href="#" class="footer__logo">
        <img src="@/assets/img/logo.png" alt="" />
      </a>

      <div
        v-for="content in contents"
        :key="content.title"
        class="footer__content"
      >
        <h3 class="footer__title">{{ content.title }}</h3>

        <ul class="footer__links">
          <li v-for="link in content.productLinks" :key="link.text">
            <a :href="link.href" class="footer__link">{{ link.text }}</a>
          </li>
        </ul>
      </div>

      <div class="footer__content">
        <form action="" class="footer__form">
          <input type="email" placeholder="Email" class="footer__input" />
          <button class="button button--flex">
            <i class="ri-send-plane-line button-icon"></i> Подписаться
          </button>
        </form>

        <div class="footer__social">
          <a
            v-for="link in socialLinks"
            :key="link.href"
            :href="link.href"
            class="footer__social-link"
            target="_blank"
          >
            <i :class="link.iconClass"></i>
          </a>
        </div>
      </div>
    </div>

    <p class="footer__copy">&#169; Никита. Все права защищены.</p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      contents: [
        {
          title: "Продукты",
          productLinks: [
            { href: "#", text: "Headphones" },
            { href: "#", text: "Earphones" },
            { href: "#", text: "Earbuds" },
            { href: "#", text: "Аксессуары" },
          ],
        },
        {
          title: "Поддержка",
          productLinks: [
            { href: "#", text: "Вопросы" },
            { href: "#", text: "Регистрация" },
            { href: "#", text: "Обновления" },
            { href: "#", text: "Обеспечение" },
          ],
        },
      ],
      socialLinks: [
        { href: "https://facebook.com/", iconClass: "ri-facebook-fill" },
        { href: "https://instagram.com", iconClass: "ri-instagram-line" },
        { href: "https://twitter.com", iconClass: "ri-twitter-line" },
      ],
    };
  },
};
</script>

<style scoped>
.footer__container {
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  row-gap: 2rem;
}

.footer__logo {
  width: 2rem;
}

.footer__title {
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  margin-bottom: 1rem;
}

.footer__links {
  display: flex;
  flex-direction: column;
  row-gap: 0.5rem;
}

.footer__link {
  color: var(--text-color);
}

.footer__link:hover {
  color: var(--white-color);
}

.footer__form {
  display: flex;
  column-gap: 0.5rem;
  background-color: var(--container-color);
  padding: 0.5rem 0.75rem;
  border-radius: 0.5rem;
  margin-bottom: 2rem;
}

.footer__input {
  background-color: var(--container-color);
  width: 90%;
  color: var(--white-color);
}

.footer__input:placeholder {
  color: var(--text-color);
  font-size: var(--normal-font-size);
  font-family: var(--body-font);
}

.footer__social {
  display: flex;
  column-gap: 1.25rem;
}

.footer__social-link {
  display: inline-flex;
  color: var(--white-color);
  background-color: var(--container-color);
  padding: 0.5rem;
  border-radius: 0.25rem;
  font-size: 1rem;
}

.footer__social-link:hover {
  background-color: var(--first-color);
}

.footer__copy {
  margin-top: 5rem;
  text-align: center;
}

@media screen and (min-width: 767px) {
  .footer__container {
    grid-template-columns: 0.4fr 0.7fr.7fr 1fr;
  }
}

@media screen and (min-width: 1024px) {
  .footer__container {
    padding-top: 3rem;
  }

  .footer__copy {
    margin-top: 9rem;
  }
}
</style>
