<script setup>
import { ref } from 'vue';
import img from "@/assets/img/cards/01.jpg"

const apartments = ref([
  {
    img: img,
    title: 'Пентхаус “Loft Олимп”',
    link: '#!',
  },
  {
    img: img,
    title: 'Апартаменты “Nice Loft”',
    link: '#!',
  },
  {
    img: img,
    title: 'Апартаменты “Loft Studio”',
    link: '#!',
  },
  {
    img: img,
    title: 'Loft квартира “Престиж”',
    link: '#!',
  }
]);
</script>

<template>
  <section class="benefits none1">
    <h2 class="visually-hidden">Преимущества ЖК</h2>

    <div class="container container--sm">
      <div class="benefits__row">

        <div class="benefits__item">
          <img src="@/assets/img/benefits/bench.svg" alt="" class="benefits__item-img">
          <p class="benefits__item-text">Рядом исторические парки&nbsp;и&nbsp;скверы</p>
        </div>

        <div class="benefits__item">
          <img src="@/assets/img/benefits/building.svg" alt="" class="benefits__item-img">
          <p class="benefits__item-text">Полностью обустроенный</p>
        </div>

        <div class="benefits__item">
          <img src="@/assets/img/benefits/fountain.svg" alt="" class="benefits__item-img">
          <p class="benefits__item-text">10 фонтанов на территории</p>
        </div>

        <div class="benefits__item">
          <img src="@/assets/img/benefits/bicycle.svg" alt="" class="benefits__item-img">
          <p class="benefits__item-text">6 км велодорожек</p>
        </div>

      </div>
    </div>

  </section>

  <section class="apartments none1">
    <div class="container">

      <div class="apartments__title">
        <h2 class="title-2">Наши квартиры</h2>
      </div>

      <div class="apartments__cards">
        <a v-for="(apartment, index) in apartments" :key="index" :href="apartment.link" class="card">
          <img class="card__img" :src="apartment.img" :alt="apartment.title">
          <h3 class="card__title">{{ apartment.title }}</h3>
        </a>
      </div>
    </div>
  </section>

  <section class="cta none1">
    <div class="container">
      <div class="cta__title">
        <h2 class="title-2">Хотите посмотреть?</h2>
      </div>
      <div class="cta__wrapper">

        <div class="cta__text">
          <p>ЖК LoftHouse – это проект бизнес-класса, расположенный в центре города, на Наб. реки Фонтанки 10-15. Комплекс предлагает своим жильцам квартиры площадью от 40 до 170 кв. м. В здании будет три секции, в которых разместится всего 56 квартир.</p>
        </div>

        <form action="" class="cta__form form">
          <input type="text" class="form__input" placeholder="Ваше имя" autocomplete="off">
          <input data-tel-input type="text" class="form__input" placeholder="Ваш телефон" autocomplete="off">

          <p class="form__privacy form__privacy--bottom">
            *Мы никому не передаем ваши данные. <br>И не сохраняем ваш номер в базу.
          </p>

          <button type="submit" class="form__btn">Посмотреть район</button>
        </form>
      </div>
    </div>
  </section>

  <section class="video none1">
    <h2 class="visually-hidden">Видео про ЖК Loft House</h2>
    <div class="container">

      <a href="https://www.youtube.com/watch?v=bhJNL9JUsnY" data-youtubeLightbox class="video__link">
        <img src="@/assets/img/video/play.svg" alt="" class="video__icon">
        <img src="@/assets/img/video/video-img.jpg" alt="" class="video__img">
      </a>
    </div>
  </section>

  <section class="section-map none1">
    <div class="container">
      <div class="section-map__title">
        <h2 class="title-2">Район на карте</h2>
      </div>
      <div class="section-map__map">
        <div class="map" id="map"></div>
      </div>
    </div>
  </section>

  <section class="feedback none1">
    <div class="container">
      <div class="feedback__title">
        <h2 class="title-2">Есть вопросы?</h2>
      </div>
      <form class="feedback__form form">

        <p class="form__privacy form__privacy--bottom">
          *Мы никому не передаем ваши данные. <br>И не сохраняем ваш номер в базу.
        </p>

        <input type="text" class="form__input" placeholder="Ваше имя" autocomplete="off">
        <input data-tel-input type="text" class="form__input" placeholder="Ваш телефон" autocomplete="off">

        <button type="submit" class="form__btn">Посмотреть район</button>
      </form>
    </div>
  </section>
</template>

<style scoped>

</style>