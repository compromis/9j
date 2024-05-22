<script setup>
const localePath = useLocalePath()
</script>

<template>
  <section class="candidates" id="candidatura" aria-labelledby="CandidatesTitle" style="background-image: url(/images/candidates.jpg)">
    <div class="container padded">
      <h2 id="CandidatesTitle" class="font-headline skew">{{ $t('candidates.title') }}</h2>
    </div>
    <SiteSlider class="candidates-cards">
      <article class="candidates-card">
        <h3 class="font-headline skew candidate-name">Vicent Marzà</h3>
        <SiteSocials
          class="candidate-socials"
          :socials="[
            { icon: 'fa6-brands:instagram', name: 'Instagram', url: 'https://www.instagram.com/vicentmarza/' },
            { icon: 'fa6-brands:tiktok', name: 'TikTok', url: 'https://www.tiktok.com/@vicentmarza' },
            { icon: 'fa6-brands:x-twitter', name: 'Twitter / X', url: 'https://x.com/VicentMarza' },
          ]"
        />
        <p class="candidate-description">
          Els últims 8 anys, he fet tant com he pogut i més per representar les polítiques de Compromís a les Corts Valencianes i al Govern del Botànic.
          <NuxtLink :to="localePath('/marza')">
            {{ $t('candidates.more_info') }}
          </NuxtLink>
        </p>
      </article>
      <article class="candidates-card">
        <h3 class="font-headline skew candidate-name">Sandra Ruiz Andrés</h3>
        <SiteSocials
          class="candidate-socials"
          :socials="[
            { icon: 'fa6-brands:instagram', name: 'Instagram', url: 'https://www.instagram.com/sandraruiz92/' },
            { icon: 'fa6-brands:tiktok', name: 'TikTok', url: 'https://www.tiktok.com/@salhanaa' },
            { icon: 'fa6-brands:x-twitter', name: 'Twitter / X', url: 'https://x.com/sandraruiz92' },
            { icon: 'fa6-brands:facebook', name: 'Facebook', url: 'https://www.facebook.com/sandra.r.andres.5/' },
          ]"
        />
      </article>
      <article class="candidates-card candidates-other">
        <h3>{{ $t('candidates.rest') }}</h3>
        <ul>
          <li class="font-headline">Yurena Hueso García</li>
          <li class="font-headline">Ioana Sintimbrean</li>
          <li class="font-headline">Patricia Sala Pareja</li>
          <li class="font-headline">Andreu Soler i Salvador</li>
          <li class="font-headline">Demetrio Gómez Ávila</li>
        </ul>
      </article>
    </SiteSlider>
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
  flex-direction: column;
  justify-content: space-between;

  .container {
    width: 100%;
  }

  h2 {
    font-size: var(--text-3xl);
    color: var(--white);
  }

  &-card {
    display: flex;
    flex-direction: column;
    gap: var(--spacer-4);
    background: var(--orange);
    color: var(--white);
    padding: var(--site-padding);
    min-height: 40vh;
    min-width: 40vw;

    .candidate-name {
      font-size: var(--text-xl);
    }

    .candidate-socials {
      :deep(a) {
        opacity: 1;

        &:hover {
          opacity: .75;
        }
      }
    }

    .candidate-description {
      font-size: var(--text-base);
      margin-block-start: auto;

      a {
        color: var(--white);
      }
    }
  }

  &-other {
    display: flex;
    flex-direction: column;
    gap: var(--site-padding);

    ul {
      list-style: none;
      margin: 0;
      padding: 0;
      margin-block-start: auto;
      border-top: 1.5px var(--white) solid;
    }

    li {
      font-size: var(--text-md);
      padding: var(--spacer-2) 0;
      border-bottom: 1.5px var(--white) solid;
    }
  }
}

@include media('<md') {
  .candidates {
    background-position: center;

    h2 {
      display: none;
    }

    &-card {
      width: 75vw;
      min-height: 30vh;
      flex-shrink: 0;
    }

    .slider {
      padding-left: var(--site-padding);
    }
  }
}
</style>