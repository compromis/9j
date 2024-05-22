<template>
  <section class="manifesto" id="programa" aria-labelledby="ProgramaTitle">
    <div class="container padded manifesto-cols">
      <h2 id="ProgramaTitle" class="font-headline skew manifesto-title">
        Programa<br>Eleccions<br>Europees<br>2024
      </h2>
      <div class="manifesto-cover">


      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.manifesto {
  background: var(--fuchsia);
  color: var(--white);
  min-height: 100vh;
  min-height: 100svh;
  padding-top: 4rem;

  h2 {
    font-size: var(--text-3xl);
    line-height: 1;
  }

  &-cols {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: var(--site-padding);
  }

  &-cover {
    background: var(--white);
  }
}
</style>