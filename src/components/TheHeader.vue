<template>
  <header class="header">
    <nav class="header__nav">
      <img class="header__hamburger" src="@/assets/hamburger.svg" alt="hamburger" />
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
  width: 38px;
  height: 100%;

  &__hamburger {
    width: 38px;
    height: 38px;
    cursor: pointer;
    transition: all 0.3s ease;
    will-change: transform;

    &:hover {
      transform: scale(1.1);
    }
  }

  &__nav {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 38px;
    width: 38px;

    position: fixed;
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
      font-size: 1.75em;
      font-weight: bold;
      font-family: "Montserrat", sans-serif;

      writing-mode: vertical-rl;
      text-orientation: mixed;
      text-transform: uppercase;
      transition: color 0.3s ease-in-out;
      will-change: color;

      &:hover {
        color: var(--color-action);
      }
    }
  }
}
</style>
