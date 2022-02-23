<template>
  <section class="about">
    <div class="about__me">
      <h1 class="about__me__title">About me</h1>
      <p class="about__me__description">
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem
        aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo
        enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos
        qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet,
        consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam
        quaerat voluptatem.
      </p>

      <button-round>See my projects</button-round>

      <p class="about__me__description">
        Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea
        commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae
        consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?
      </p>

      <ul class="about__me__languages">
        <li>SCALA</li>
        <li>PYTHON</li>
        <li>PHP</li>
        <li>APL</li>
        <li>ASSEMBLY</li>
        <li>PASCAL</li>
        <li>IOTA</li>
        <li>BINARY</li>
      </ul>
    </div>
    <div class="about__details">
      <!--placeholder-->
    </div>
  </section>
</template>

<script>
import ButtonRound from "@/components/ButtonRound";

export default {
  name: "TheAbout",
  components: { ButtonRound },
};
</script>

<style lang="scss" scoped>
.about {
  height: 90vh;
  border-left: 2px solid var(--color-elment);
}
</style>
