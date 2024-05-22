<script setup>
const compromis = [
  { icon: 'fa6-brands:instagram', name: 'Instagram', url: 'https://instagram.com/compromis' },
  { icon: 'fa6-brands:tiktok', name: 'TikTok', url: 'https://tiktok.com/@compromis_net' },
  { icon: 'fa6-brands:x-twitter', name: 'Twitter / X', url: 'https://twitter.com/compromis' },
  { icon: 'fa6-brands:youtube', name: 'YouTube', url: 'https://youtube.com/coaliciocompromis' },
  { icon: 'fa6-brands:facebook', name: 'Facebook', url: 'https://facebook.com/coaliciocompromis' },
  { icon: 'fa6-brands:whatsapp', name: 'Facebook', url: 'https://comprom.is/whatsapp' },
  { icon: 'fa6-brands:telegram', name: 'Facebook', url: 'https://t.me/s/compromis' },
]

const sumar = [
  { icon: 'fa6-brands:instagram', name: 'Instagram', url: 'https://www.instagram.com/sumar_oficial/' },
  { icon: 'fa6-brands:tiktok', name: 'TikTok', url: 'https://www.tiktok.com/@sumar_oficial' },
  { icon: 'fa6-brands:x-twitter', name: 'Twitter / X', url: 'https://twitter.com/sumar' },
  { icon: 'fa6-brands:youtube', name: 'YouTube', url: 'https://www.youtube.com/@sumar_oficial' },
  { icon: 'fa6-brands:facebook', name: 'Facebook', url: 'https://www.facebook.com/SumarOficial2022/' },
]
</script>

<template>
  <footer class="footer">
    <div class="container padded">
      <div class="footer-compromis">
        <SiteLogoCompromis class="footer-logo" />
        <SiteSocials :socials="compromis" />
      </div>
      <div class="footer-sumar">
        <SiteLogoSumar class="footer-logo" />
        <SiteSocials :socials="sumar" />
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  .container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: var(--site-padding);
  }

  &-logo {
    height: 2rem;
  }

  &-compromis,
  &-sumar {
    display: flex;
    flex-direction: column;
  }

  &-compromis {
    align-items: flex-start;
  }

  &-sumar {
    align-items: flex-end;
  }
}

@include media('<md') {
  .footer {
    .container {
      grid-template-columns: 1fr;
      padding-bottom: 5rem;
    }

    &-sumar {
      align-items: flex-start;
      margin-top: 2rem;
    }
  }
}
</style>