<template>
  <section class="hero">
    <the-auto-scroll />
    <div class="hero__content">
      <div class="sonna">
        <!--placeholder-->
      </div>
      <div class="intro">
        <!--placeholder-->
      </div>
      <div class="details">
        <!--placeholder-->
      </div>
      <div class="socials">
        <!--placeholder-->
      </div>
    </div>
  </section>
</template>

<script>
import TheAutoScroll from "@/components/TheAutoScroll";
export default {
  name: "TheHero",
  components: { TheAutoScroll },
};
</script>

<style lang="scss" scoped>
.hero {
  display: flex;
  align-items: center;

  width: 100%;
  height: 100vh;

  &__content {
    height: 100%;
    width: 100%;
    background: rgba(0, 0, 0, 0.5);
    border-left: 2px solid var(--color-elment);
  }
}
</style>
