<script setup lang="ts">
    const { slug } = useRoute().params
</script>

<template>
    <article class="bg-white rounded-2xl">
        <ContentDoc :path="`/${slug}`" v-slot="{ doc }">
            <header>
                <div class="text-center p-5">
                <h1 class="text-4xl font-semibold">{{ doc.title }}</h1>
                <div class="text-gray-500 text-sem mt-2">{{ doc.date }}</div>
            </div>

            
            <div class="h-[320px] relative">
                <img :src="doc.thumbnail" alt="" class="w-full h-full object-cover absolute">
                </div>
            </header>

            <!-- Content -->
            <div class="content">
                <!-- Usamos o content renderer para renderizar o arquivo .md, é um equivalente do v-html, mas criado pelo Nuxt -->
                <ContentRenderer :value="doc"></ContentRenderer>
            </div>
        </ContentDoc>
    </article>
</template>

<style>
    .content p:not(:last-child),
    .content li:not(:last-child),
    .content blockquote:not(:last-child),
    .content h1:not(:last-child),
    .content h2:not(:last-child),
    .content h3:not(:last-child),
    .content h4:not(:last-child),
    .content pre:not(:last-child),
    .content table:not(:last-child) {
        @apply mb-4
    }

    .content h1 {
        @apply text-3xl font-bold
    }
    .content h2 {
        @apply text-2xl font-bold
    }
    .content h3 {
        @apply text-xl font-bold
    }

</style> -->