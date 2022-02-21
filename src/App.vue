<template>
  <the-header />
  <main class="main">
    <the-hero />
    <section class="about">
      <div class="about__me">
        <!--placeholder-->
      </div>
      <div class="about__details">
        <!--placeholder-->
      </div>
    </section>
    <section class="history"></section>
    <section class="projects"></section>
  </main>
</template>

<script>
import TheHeader from "@/components/TheHeader";
import TheHero from "@/components/TheHero";

export default {
  components: {
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
}

a {
  color: inherit;
  text-decoration: none;
}
</style>
