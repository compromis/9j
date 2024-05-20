<script setup>
const { locale, locales } = useI18n()

const menu = [
  { label: 'menu.proposals', href: '#propostes', color: 'orange' },
  { label: 'menu.candidates', href: '#candidatura', color: 'fuchsia' },
  { label: 'menu.manifesto', href: '#programa', color: 'white' },
  { label: 'menu.collaborate', href: '#collabora', color: 'orange' }
]

const { $emit } = useNuxtApp()

const color = ref('blue')

function changeHeroBackground (newColor) {
  $emit('changeHeroBackground', newColor)
  color.value = newColor
} 

function reset () {
  $emit('changeHeroBackground', 'blue')
  color.value = 'blue'
}
</script>

<template>
  <header :class="['nav', `links-${color}`]">
    <div class="container padded">
      <div class="nav-logos">
        <a href="https://compromis.net" target="_blank">
          <SiteLogoCompromis />
        </a>
        <a href="https://movimientosumar.es" target="_blank">
          <SiteLogoSumar />
        </a>
      </div>
      <nav class="nav-menu font-headline" label="Menú principal">
        <ul class="nav-list list-reset">
          <li v-for="(item, i) in menu" :key="i">
            <a :href="item.href" @mouseenter="changeHeroBackground(item.color)" @mouseleave="reset">
              {{ $t(item.label) }}
            </a>
          </li>
        </ul>
      </nav>
      <ul class="nav-languages nav-list list-reset font-headline">
        <li v-for="lang in locales" :key="lang.code">
          <SwitchLocalePathLink
            :locale="lang.code"
            :aria-label="$t('assist.language', { lang: lang.name })"
          >
            {{ lang.code }}
          </SwitchLocalePathLink>
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.nav  {
  position: fixed;
  top: 0;
  left: var(--site-padding);
  right: var(--site-padding);
  z-index: 1000;

  .container {
    background: var(--white);
    display: flex;
    gap: var(--spacer-8);
    padding: var(--spacer-5);
  }

  &-logos {
    display: flex;
    gap: var(--spacer-8);

    :deep(svg) {
      display: block;
      height: 1.75rem;
      width: auto;
    }
  }

  &-menu {
    display: flex;
    align-items: center;
    margin-inline: auto;

    li {
      display: flex;
      margin-block: calc(var(--spacer-4) * -1);
    }

    li:hover a {
      transform: skew(-3deg, -3deg);
      text-decoration: underline;
    }

    a {
      display: flex;
      color: var(--link-color, var(--blue));
      transition: .25s ease;
      height: 100%;
      padding-block: var(--spacer-4);
    }
  }

  &-list {
    display: flex;
    align-items: center;
    gap: var(--spacer-4);
    font-size: var(--text-md);
    line-height: 1;

    :deep(a) {
      text-decoration: none;
    }
  }

  &-languages {
    gap: 0;
    margin-block: calc(var(--spacer-2) * -1);

    :deep(a) {
      font-size: var(--text-base);
      text-transform: uppercase;
      padding: var(--spacer-2);
      display: block;

      &.router-link-active {
        background: var(--orange);
        color: var(--white);
      }

      &:not(.router-link-active):hover {
        background: rgba($orange, .15);
      }
    }
  }
}

.links-orange {
  --link-color: var(--fuchsia);
}

.links-white {
  --link-color: var(--blue);
}

.links-fuchsia {
  --link-color: var(--orange);
}

@include media('<lg') {
  .nav {
    .container {
      justify-content: space-between;
    }

    &-logos {
      gap: var(--spacer-2);

      svg {
        height: 1rem;
      }
    }

    &-menu {
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      overflow: auto;
      background: var(--white);

      li {
        margin: 0;
      }

      a {
        display: block;
        padding: var(--spacer-4);
      }
    }
  }
}
</style>