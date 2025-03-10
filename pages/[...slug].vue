<script lang="ts" setup>
    const route = useRoute()

    const { data: post } = await useAsyncData(() => {
        return queryCollection('content')
        .path(route.path)
        .first()
    })
</script>

<template>
    <article>
        <nuxt-link to="/">
            <small>« Back </small>
        </nuxt-link>

        <h1 class="text-2xl">{{ post.title }}</h1>
        <div>{{ post.date }}</div>
        
        <div class="flex flex-wrap gap-3 mb-4">
            <span class="text-lime-400 hover:underline hover:text-lime-700 cursor-pointer" 
            v-for="tag in post.tags" 
            :key="tag">#{{ tag }} </span>
        </div>

        <ContentRenderer :value="post" />
    </article>
</template>

<style>
    article p:not(:last-child),
    article li:not(:last-child),
    article blockquote:not(:last-child),
    /* article h1:not(:last-child), */
    article h2:not(:last-child),
    article h3:not(:last-child),
    article h4:not(:last-child),
    article pre:not(:last-child),
    article table:not(:last-child) {
        @apply mb-4
    }
    article pre{
        @apply bg-gray-300 opacity-80 rounded-md p-3
    }
</style>