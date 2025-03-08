<!-- <script setup lang="ts">
const { data: home } = await useAsyncData(() => queryCollection('content').path('/').first())

useSeoMeta({
  title: home.value?.title,
  description: home.value?.description
})
</script>

<template>
  <ContentRenderer v-if="home" :value="home" />
  <div v-else>Home not found</div>
</template> -->

<script setup lang="ts">
const { data: posts } = await useAsyncData('blog', () => queryCollection('content').all())
</script>

<template>
    <div>
        <h1 class="text-2xl font-semibold">Blog</h1>
        <ul>
            <li v-for="post in posts" :key="post.id">
                <NuxtLink :to="post.path">{{ post.title }}</NuxtLink>
                <p class="text-base"> {{ post.description }}</p>
            </li>
        </ul>
    </div>
</template>
