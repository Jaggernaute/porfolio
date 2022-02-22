<template>
  <the-header />
  <main class="main">
    <the-hero />
    <the-about />
    <section class="history"></section>
    <section class="projects"></section>
  </main>
</template>

<script>
import TheHeader from "@/components/TheHeader";
import TheHero from "@/components/TheHero";
import TheAbout from "@/components/TheAbout";

export default {
  components: {
    TheAbout,
    TheHeader,
    TheHero,
  },
};
</script>

<style lang="scss">
:root {
  --color-bg: #373e48;
  --color-text: #f6faff;
  --color-elment: var(--color-text);
  --color-action: #ef8d8d;
}

body {
  margin: 0;

  color: var(--color-text);
  background: var(--color-bg);

  font-family: "Poppins", sans-serif;
  font-size: 14px;
}

#app {
  position: relative;
  width: 1422px;
  margin: 0 auto;
}

.main {
  min-height: 200vh;
  border-right: 2px solid var(--color-elment);
  width: calc(100% - 70px);

  & > section {
    position: relative;
    width: 100%;

    &::after {
      content: "";
      height: 2px;
      width: 100vw;
      right: 0;
      bottom: -2px;
      position: absolute;
      background: var(--color-elment);
    }
  }
}

a {
  color: inherit;
  text-decoration: none;
}
</style>
