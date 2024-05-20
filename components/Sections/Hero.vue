<script setup>
const color = ref('blue')
const { $on, $gsap } = useNuxtApp()

onMounted(() => {
  $on('changeHeroBackground', (newColor) => {
    color.value = newColor

    $gsap.to(`.hero-backgrounds > div:not(.background-${newColor})`, {
      x: '110%',
      duration: 1.5,
      skewX: '15deg',
      ease: "expo.out",
    })

    $gsap.to(`.background-${newColor}`, {
      x: '-10%',
      skewX: '5deg',
      duration: 1.5,
      ease: "expo.out",
    })
  })
})
</script>

<template>
  <section :class="['hero', `color-${color}`]">
    <div class="hero-content">
      <SiteEuroPV class="euro-pv" />
      <SiteSlogan class="slogan" />
    </div>
    <div class="hero-backgrounds">
      <div class="background-orange" />
      <div class="background-fuchsia" />
      <div class="background-blue" />
      <div class="background-white" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.hero {
  position: relative;
  background: var(--blue);
  color: var(--white);
  min-height: 100vh;
  min-height: 100svh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: var(--site-padding);
  padding-top: var(--navbar-safe-area);
  overflow: clip;

  &-content {
    display: flex;
    position: relative;
    z-index: 50;
    flex-direction: column;
    gap: 2vh;
  }

  :deep(svg) {
    transition: .25s ease;
  }
}

.slogan {
  height: calc(10vh + 10rem);
  max-width: 100%;
}

.euro-pv {
  height: calc(15vh + 10rem);
}

.hero-backgrounds > div {
  position: absolute;
  inset: 0;
  width: 120vw;
  transform: translateX(110%) skewX(15deg);
}

.background-orange {
  background-color: var(--orange);
  z-index: 10 !important;
}

.background-fuchsia {
  background-color: var(--fuchsia);
  z-index: 10;
}

.background-blue {
  background-color: var(--blue);
  z-index: 1;
}

.background-white {
  background-color: var(--white);
  z-index: 10;
}

.color-white {
  color: var(--blue);
}
</style>