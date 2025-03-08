<script setup lang="ts">
const { data: posts } = await useAsyncData(() => queryCollection('content').all())
// const { data: posts } = await useAsyncData('blog', () => queryContent().find())
console.log(posts)
</script>

<template>
  <div>
    <h1>Blog</h1>
    <!-- <ul>
      <li v-for="post in posts" :key="post.id">
        <NuxtLink :to="post.path">{{ post.title }} - {{ post.date }}</NuxtLink>
      </li>
    </ul> -->
    <ContentList path="/" v-slot="{ list }" :query="{
      draft: false,
      sort: [{ date: -1 }]
    }">
      <div v-for="post in list" :key="post._path">
        <div class="text-sm text-gray-500 mt-px">{{ post.title }}</div>
        <div class="text-sm text-gray-500 mt-px">{{ post.date }}</div>
      </div>
    </ContentList>
  </div>
</template>
