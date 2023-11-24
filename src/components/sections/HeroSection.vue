<template>
  <section class="hero-section">
    <div class="hero-section__tob-bar">
      <img :src="logoSrc" alt="logo">

      <nav class="hero-section__nav">
        <a>Головна</a>
        <a>Послуги</a>
        <a>Наша команда</a>
        <a>Контакти</a>
      </nav>
    </div>

    <div class="hero-section__body">
      <div class="hero-section__left">
        <div class="hero-section__chip">
          <div class="hero-section__line" /> Україна, Кременчук
        </div>

        <h1>
          Зробимо все
          <br>
          заради вашої
          <br>

          <span>
            краси
          </span>
        </h1>

        <button>
          Записатися
        </button>
      </div>
      <div class="hero-section__right">
        <img :src="personSrc" alt="person" />
        <div class="hero-section__bg-object" />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import logoSrc from '@/assets/png/logo.webp'
import personSrc from '@/assets/png/person.webp'

</script>

<style lang="scss">
.hero-section {
  display: grid;
  grid-row-gap: 20px;
  grid-template-rows: auto 1fr;
}
.hero-section__nav {
  display: grid;
  grid-auto-flow: column;
  grid-column-gap: 40px;
  justify-self: end;
  a {
    color: var(--app-text-primary-color);
  }
}

.hero-section__body {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-column-gap: 20px;
}
.hero-section__left {
  display: grid;
  align-self: center;
  grid-template-rows: min-content min-content;
  height: 100%;
  align-content: center;
  h1 {
    margin: 16px 0 32px;
    font-weight: 600;
    color: var(--app-text-secondary-color);

    span {
      position: relative;
      color: var(--app-text-primary-color);
      width: min-content;
      &:after {
        content: "";
        display: block;
        height: 4px;
        left: 2px;
        width: calc(100% - 4px);
        background-color: var(--app-text-primary-color);
        position: absolute;
        bottom: 10px;
      }
    }
  }
}

.hero-section__tob-bar {
  display: grid;
  grid-template-columns: auto 1fr;
  align-items: center;

  img {
    height: 60px;
    width: auto;
  }
}

.hero-section__chip {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-column-gap: 30px;
  align-items: center;
  color: var(--app-text-primary-color);
}
.hero-section__line {
  height: 1px;
  background-color: var(--app-text-primary-color);
  width: 150px;
}

.hero-section__right {
  position: relative;

  img {
    position: absolute;
    height: 100%;
    width: auto;
    bottom: -20px;
    z-index: 3;
  }
}

.hero-section__bg-object {
  width: 100%;
  background-color: var(--app-text-secondary-color);
  height: 90%;
  align-self: end;
  position: absolute;
  bottom: -20px;
  right: 0;
  border-top-right-radius: 40%;
  border-top-left-radius: 40%;
  z-index: 2;
}
</style>
