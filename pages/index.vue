<template>
    <div>
        <!-- query é uma série de atributos que podemos utilizar para a cahamda do nosso arqui, no "sort" estamos criando um tipo de filtro para sempre mostrar os posts por data -->
        <ContentList 
            path="/content" v-slot="{ list }"
            :query="{
                draft:false,
                sort: [{date: -1}]
            }">

            <div 
            v-for="post in list" :key="post._path"
            class="blog-card bg-white rounded-2xl overflow-hidden mb-4">
                <div class="h-[320px] relative">
                    <img :src="post.thumbnail" alt="" class="w-full h-full absolute object-cover">
                </div>

                <div class="blog-card--meta">
                    <h3 class="text-2xl font-semibold">
                        <NuxtLink :to="`/${post.slug}`">{{ post.title }}</NuxtLink> 
                    </h3>
                    
                    <div class="text-sm text-gray-500 mt-px">{{ post.date }}</div>
                </div>
            </div>
        </ContentList> 
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped>

</style>