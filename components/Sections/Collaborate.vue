<template>
  <section class="collaborate" id="collabora" aria-labelledby="CollaboraTitle">
    <div class="container padded collaborate-cols">
      <h2 id="CollaboraTitle" class="font-headline skew">{{ $t('collaborate.title') }}</h2>
      <article class="collaborate-card color-orange">
        <h3 class="font-headline">{{ $t('collaborate.donate.title') }}</h3>
        <p>{{ $t('collaborate.donate.text') }}</p>

        <ul class="collaborate-links">
          <li>
            <a href="https://donacions.compromis.net/donate/10" target="_blank">10€</a>
          </li>
          <li>
            <a href="https://donacions.compromis.net/donate/25" target="_blank">25€</a>
          </li>
          <li>
            <a href="https://donacions.compromis.net/donate/50" target="_blank">50€</a>
          </li>
          <li>
            <a href="https://donacions.compromis.net/donate/100" target="_blank">100€</a>
          </li>
          <li>
            <a href="https://donacions.compromis.net" target="_blank">{{ $t('collaborate.donate.other') }}</a>
          </li>
        </ul>
      </article>
      <article class="collaborate-card color-fuchsia">
        <h3 class="font-headline">{{ $t('collaborate.interventor.title') }}</h3>
        <p>{{ $t('collaborate.interventor.text') }}</p>

        <ul class="collaborate-links">
          <li>
            <a href="https://apoderats.compromissumar.net/" target="_blank">{{ $t('collaborate.interventor.cta') }}</a>
          </li>
        </ul>
      </article>
      <article class="collaborate-card color-blue">
        <h3 class="font-headline">{{ $t('collaborate.amplify.title') }}</h3>
        <p>{{ $t('collaborate.amplify.text') }}</p>

        <ul class="collaborate-links">
          <li>
            <a href="https://apoderats.compromissumar.net/" target="_blank">Instagram</a>
          </li>
          <li>
            <a href="https://apoderats.compromissumar.net/" target="_blank">TikTok</a>
          </li>
          <li>
            <a href="https://apoderats.compromissumar.net/" target="_blank">X</a>
          </li>
          <li>
            <a href="https://apoderats.compromissumar.net/" target="_blank">Facebook</a>
          </li>
        </ul>
      </article>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.collaborate {
  display: flex;
  background: var(--blue);
  color: var(--white);
  min-height: 100vh;
  min-height: 100svh;
  padding-top: 4rem;

  h2 {
    font-size: var(--text-3xl);
  }

  &-cols {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: var(--site-padding);
  }

  &-card {
    background: var(--white);
    color: var(--blue);
    padding: var(--site-padding);
    display: flex;
    flex-direction: column;
    gap: var(--site-padding);

    h3 {
      font-size: var(--text-lg);
      margin: 0;
    }

    p {
      font-size: var(--text-base);
      margin: 0;
    }
  }

  &-links {
    display: flex;
    flex-wrap: wrap;
    gap: var(--spacer-4);
    list-style: none;
    padding: 0;
    margin: 0;
    margin-block-start: auto;

    a {
      display: block;
      background: var(--color);
      color: var(--white);
      padding: .5em .75em;
      font-weight: bold;
      font-family: var(--font-headline);
      text-decoration: none;
      font-size: var(--text-md);
      border: 3px var(--color) solid;

      &:hover {
        background: var(--white);
        color: var(--color);
      }
    }
  }
}

@include media('<md') {
  .collaborate {
    h2 {
      margin-block-end: var(--spacer-8);
    }

    &-cols {
      grid-template-columns: 1fr;
    }
  }
}
</style>