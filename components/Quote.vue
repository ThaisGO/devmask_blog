<script setup>
    defineProps(['icon'])
</script>

<template>
    <div class="flex items-center gap-4 bg-zinc-900 text-lime-400 text-base mb-3 p-4 rounded-md">
        <div>
            <i :class="[icon]"></i>
        </div> 
        <slot mdc-unwrap="p" />
    </div>
</template>