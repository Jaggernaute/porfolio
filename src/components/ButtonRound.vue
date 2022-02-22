<template>
  <div class="btn">
    <a class="btn__text" :href="href">
      <slot></slot>
    </a>
  </div>
</template>

<script>
export default {
  name: "ButtonRound",
  props: {
    href: {
      type: String,
      default: "#",
    },
  },
};
</script>

<style lang="scss" scoped>
.btn {
  transition: all 0.5s ease-in-out;
  position: relative;

  height: 38px;

  display: flex;
  align-items: center;
  justify-content: center;

  color: var(--color-text);
  background-color: transparent;
  z-index: 0;

  &__text {
    transition: all 0.5s ease-in-out;
    font-family: Poppins, serif;
    font-style: normal;
    font-weight: 500;
    font-size: 1.2em;
  }

  &::before {
    transition: all 0.5s ease-in-out;
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: end;
    content: ">";
    font-family: Poppins, serif;
    font-weight: 900;
    font-size: 2em;
    background-color: var(--color-bg);

    height: 38px;

    left: calc(100% + 10px);
    right: -48px;
    z-index: -1;
    padding: 0 12px;
    border-radius: 38px;
  }

  &:hover {
    color: var(--color-bg);

    &::before {
      width: auto;
      left: -12px;
      background-color: var(--color-elment);
      color: var(--color-bg);
    }
    &__text {
      color: var(--color-bg);
    }
  }
}
</style>
