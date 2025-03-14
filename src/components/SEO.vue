<template>
  <div></div>
</template>

<script setup>
import { watch, onMounted } from 'vue'
import { useI18n } from 'vue-i18n'

const { t, locale } = useI18n()

const updateMetaTags = () => {
  document.title = t('seo.title')

  const metaDescription = document.querySelector('meta[name="description"]')
  if (metaDescription) {
    metaDescription.setAttribute('content', t('seo.description'))
  }

  const ogTitle = document.querySelector('meta[property="og:title"]')
  if (ogTitle) {
    ogTitle.setAttribute('content', t('seo.ogTitle'))
  }

  const ogDescription = document.querySelector('meta[property="og:description"]')
  if (ogDescription) {
    ogDescription.setAttribute('content', t('seo.ogDescription'))
  }

  document.documentElement.setAttribute('lang', locale.value) // Ändert HTML `lang`
}

watch(locale, updateMetaTags, { immediate: true }) // Aktualisiert bei Sprachwechsel
onMounted(updateMetaTags) // Setzt Meta-Tags beim Laden
</script>
