<template>
  <header class="header">
    <div class="header__hamburger"></div>
    <nav class="header__nav">
      <ul class="header__nav__list">
        <li class="header__nav__item">
          <a class="header__nav__link" href="#">home</a>
        </li>
        <li class="header__nav__item">
          <a class="header__nav__link" href="#">about</a>
        </li>
        <li class="header__nav__item">
          <a class="header__nav__link" href="#">history</a>
        </li>
        <li class="header__nav__item">
          <a class="header__nav__link" href="#">project</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "TheHeader",
};
</script>

<style lang="scss" scoped>
.header {
  position: absolute;
  right: 0;
  width: 70px;

  &__nav {
    position: fixed;
    width: 70px;
    top: 26px;

    &__list {
      display: flex;
      flex-direction: column;
      list-style: none;
      align-items: center;
      gap: 68px;

      height: 80vh;
      margin: 0;
      padding: 0;
    }

    &__item {
      text-transform: uppercase;

      font-size: 1.75em;
      font-family: "Montserrat", sans-serif;

      writing-mode: vertical-rl;
      text-orientation: mixed;
    }
  }
}
</style>
