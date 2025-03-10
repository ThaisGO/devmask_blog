<script setup>
    defineProps(['image', 'alt'])
</script>

<template>
    <div v-if="image" class="max-w-[440px] h-[340px] relative  mx-auto my-8">
        <img class="w-full h-full absolute object-cover"
            :src="image"
            :alt="alt">
    </div>
</template>