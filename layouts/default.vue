<template>
    <div class="container mx-auto max-w-7xl">
        <header class="flex justify-between items-center py-4 mt-4 border-b ">
          <div class="flex items-center md:space-x-20">
            <div>
                <NuxtLink to="/" class="text-3xl font-semibold ">Sanya Lapidjio</NuxtLink>
            </div>
          
           <Menu />
          </div>

          <ClientOnly>
            <ColorModeSelector />
          </ClientOnly>
        </header>

        <main class="py-4">
            <slot />
        </main>
      
    </div>
</template>

<script setup>
useHead({
    titleTemplate: '%s - Sanya Lapidjio',
    link: [
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com'
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Roboto&display=swap',
      crossorigin: ''
    }
  ]
})
</script>


<style lang="postcss">
body {
  font-family: 'Roboto', sans-serif;
}

body {
  @apply bg-white dark:bg-gray-900 text-gray-700 dark:text-gray-300;
}

</style>