<template>
  <header class="header none1">
    <div class="header__top">
      <div class="container">
        <div class="header__top-row">
          <a href="#!">
            <img src="@/assets/img/logo.svg" alt="LoftHouse">
          </a>
          <div class="header__nav">
            <nav class="nav">
              <ul class="nav__list">
                <li><a href="#!">О комплексе</a></li>
                <li><a href="#!">Район</a></li>
                <li><a href="#!">Каталог квартир</a></li>
                <li><a href="#!">Ипотека</a></li>
                <li><a href="#!">Контакты</a></li>
              </ul>
            </nav>
          </div>

          <div class="header__nav-btn">
            <button class="nav-icon-btn" @click="toggleNav">
              <div :class="['nav-icon', { 'nav-icon--active': isActive }]"></div>
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <h1 class="header__title">
        Жилой комплекс <br>
        в историческом центре
        <a href="#benefits">
          <img
              src="@/assets/img/header/mouse.svg"
              alt="Scroll next"
              class="header__title-icon"
          >
        </a>
      </h1>
    </div>

    <div class="header__footer">
      <div class="text-right">
        <a href="#section-map" class="info info--map">Наб. реки Фонтанки 10-15</a>
      </div>
      <a href="tel:+78121234567" class="info info--tel">8 (812) 123-45-67</a>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';

const isActive = ref(false);
const isMobileNavOpen = ref(false);

const toggleNav = () => {
  isActive.value = !isActive.value;
  isMobileNavOpen.value = !isMobileNavOpen.value;
  document.body.classList.toggle('no-scroll', isMobileNavOpen.value);
};
</script>

<style scoped>

</style>