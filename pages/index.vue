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
