<script setup>
const { t } = useI18n()

const title = t('meta.title')
const description = t('meta.description')
const ogImage = t('meta.image')
const keywords = t('meta.keywords')
const themeColor = '#fff'
const twitterSite = '@compromis'

useServerSeoMeta({
  title,
  ogTitle: title,
  description,
  ogDescription: description,
  ogImage,
  twitterCard: 'summary_large_image',
  keywords,
  ogSiteName: title,
  themeColor,
  twitterSite,
  ogType: 'website',
  ogLocale: 'ca'
})
useHead({ title })
</script>

<template>
  <main class="main-site">
    <SectionsHero />
    <SectionsProposals />
    <SectionsCandidates />
    <SectionsManifesto />
    <SectionsCollaborate/>
  </main>
</template>
