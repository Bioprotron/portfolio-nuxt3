<template>
    <section class="not-prose">      
      <ul v-for="post in posts" :key="post._path">
        <li>
          <NuxtLink :to="post._path">{{ post.title }}</NuxtLink>
        </li>
      </ul>
    </section>
  </template>
  
  <script setup>
      const {data: posts} = await useAsyncData('blog-list', () => queryContent('/blog').where({_path: { $ne: '/blog' }}).only(['title', '_path']).find())
      console.log(posts)
  </script>
  
  
  
  
  <style lang="scss" scoped>
  
  </style>