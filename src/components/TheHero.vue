<template>
  <section class="hero">
    <the-auto-scroll />
    <div class="hero__content">
      <div class="sonna">
        <!--placeholder-->
      </div>
      <div class="intro">
        <ButtonRound>Explore</ButtonRound>
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
import ButtonRound from "@/components/ButtonRound";

export default {
  name: "TheHero",
  components: { ButtonRound, TheAutoScroll },
};
</script>

<style lang="scss" scoped>
.hero {
  display: flex;
  align-items: center;
  height: 100vh;

  &__content {
    height: 100%;
    width: 100%;
    background: rgba(0, 0, 0, 0.5);
    border-left: 2px solid var(--color-elment);
  }
}

// temp
.intro {
  display: grid;
  place-items: center;
  width: 100%;
  height: 100%;
}
</style>
