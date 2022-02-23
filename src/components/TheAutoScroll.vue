<template>
  <div class="auto-scroll">
    <div class="auto-scroll__move">
      <div class="text">Software Developer</div>
      <div class="text text--outlined">Software Developer</div>
      <div class="text">Software Developer</div>
      <div class="text text--outlined">Software Developer</div>
    </div>
    <div class="auto-scroll__move">
      <div class="text">Software Developer</div>
      <div class="text text--outlined">Software Developer</div>
      <div class="text">Software Developer</div>
      <div class="text text--outlined">Software Developer</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TheAutoScroll",
};
</script>

<style lang="scss" scoped>
.auto-scroll {
  user-select: none;

  display: flex;
  align-items: center;
  gap: 20px;

  writing-mode: vertical-rl;
  text-orientation: mixed;

  width: 70px;
  height: calc(100vh - 52px);
  overflow: hidden;

  &__move {
    display: flex;
    gap: 20px;

    animation: auto-scroll 10s linear infinite;
  }
}

.text {
  font-size: 1.75em;
  font-weight: bold;
  font-family: "Montserrat", sans-serif;
  height: max-content;
  transform: rotate(180deg);

  &--outlined {
    color: var(--color-bg);
    text-shadow: -2px -2px 0 var(--color-text), 2px -2px 0 var(--color-text), -2px 2px 0 var(--color-text),
      2px 2px 0 var(--color-text);
  }
}

@keyframes auto-scroll {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-100%);
  }
}
</style>
