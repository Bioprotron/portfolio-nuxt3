<template>
    <div>
        <h1>hello from the main page!</h1>
    </div>
</template>

<script setup>
    useSeoMeta({
  title: 'Main page',
  description: 'This is the main page',  
  ogTitle: 'Main page',
  ogDescription: '[og:description]',
  ogImage: '[og:image]',
  ogUrl: '[og:url]',
  portfolioTitle: 'Main page',
  portfolioDescription: '[portfolio:description]',
  portfolioImage: '[portfolio:image]',
  portfolioCard: 'summary'
})

useHead({
  htmlAttrs: {
    lang: 'en'
  },
  link: [
    {
      rel: 'icon',
      type: 'image/png',
      href: '/favicon.png'
    }
  ]
})
</script>

<style lang="scss" scoped>

</style>

