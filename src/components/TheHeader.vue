<template>
  <header class="header" :class="{ open: isMenuOpen, closed: !isMenuOpen }">
    <nav class="header__nav">
      <img @click="toggleMenu" class="header__hamburger" src="@/assets/hamburger.svg" alt="hamburger" />
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
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
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
    transition: transform 0.5s ease;
    will-change: transform;
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

      margin: 0;
      padding: 0;

      transform-origin: top;
      transition: height 0.5s ease-in-out;
    }

    &__item {
      transform-origin: top;
      transition: color 0.3s ease-in-out, transform 0.5s ease-in-out;
      will-change: color, height;
      overflow: hidden;

      font-size: 1.75em;
      font-weight: bold;
      font-family: "Montserrat", sans-serif;

      writing-mode: vertical-rl;
      text-orientation: mixed;
      text-transform: uppercase;

      &:hover {
        color: var(--color-action);
      }
    }
  }
}

.closed .header {
  &__hamburger {
    transform: rotate(135deg);
  }

  &__nav {
    &__list {
      transition: 1s ease-in-out;
      height: 20vh;
    }
  }
}

.open .header {
  &__hamburger {
    transform: rotate(0deg);
  }

  &__nav {
    &__list {
      height: 80vh;
    }
  }
}
</style>
