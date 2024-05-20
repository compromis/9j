<template>
  <section class="candidates" id="candidatura" aria-labelledby="CandidatesTitle" style="background-image: url(/images/candidates.jpg)">
    <div class="container">
      <h2 id="CandidatesTitle" class="font-headline skew">{{ $t('candidates.title') }}</h2>
      <div class="candidates-cards">
        <article class="candidates-card">
          <h3 class="font-headline skew candidate-name">Vicent Marzà</h3>
        </article>
        <article class="candidates-card">
          <h3 class="font-headline skew candidate-name">Sandra Ruiz Andrés</h3>
        </article>
        <article class="candidates-card">
          <h3>Resta de la llista</h3>
          <ul>
            <li class="font-headline">Yurena Hueso García</li>
            <li class="font-headline">Ioana Sintimbrean</li>
            <li class="font-headline">Patricia Sala Pareja</li>
            <li class="font-headline">Andreu Soler i Salvador</li>
            <li class="font-headline">Demetrio Gómez Ávila</li>
          </ul>
        </article>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
.candidates {
  background: var(--orange);
  min-height: 100vh;
  min-height: 100svh;
  background-size: cover;
  padding-top: 2rem;
  display: flex;

  h2 {
    font-size: var(--text-3xl);
    color: var(--white);
    padding-inline: var(--site-padding);
  }

  .container {
    display: flex;
    min-height: calc(2rem - 100vh);
    min-height: calc(2rem - 100vh);
    width: 100%;
    flex-direction: column;
    justify-content: space-between;
    padding-right: 0;
  }

  &-cards {
    display: flex;
    gap: var(--site-padding);
    overflow: auto;
    padding: var(--site-padding);
  }

  &-card {
    background: var(--orange);
    color: var(--white);
    padding: var(--site-padding);
    min-height: 40vh;
    min-width: 40vw;

    .candidate-name {
      font-size: var(--text-xl);
    }
  }
}
</style>