<script setup lang="ts">
  const { data: posts } = await useAsyncData(() => queryCollection('content').order('date', 'DESC').all())

  console.log('path', posts.path)
</script>

<template>
  <main class="mx-auto flex flex-col">
    <div v-for="post in posts" :key="post.id">
      <div class="flex gap-4 mb-6">
        
        <div class="text-lg font-light">
          {{ post.date }}
        </div>
        <div>
          <NuxtLink class="text-lg text-lime-500 font-medium"     
            :to="post.path">
              {{ post.category ? `[${post.category}]` : '' }} 
              {{ post.title }}
          </NuxtLink>
          <p class="text-base font-light">{{ post.description }}</p>
        </div>
      </div>
    </div>

  </main>
</template>
