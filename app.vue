<script setup lang="ts">
import { Separator } from '@/components/ui/separator'
</script>

<template>
  <div class="container">
    <header>
      <nav class=" p-4">
        <ul class="flex justify-end">
          <li><i class='bx bx-search-alt-2 text-3xl text-lime-500'></i></li>
          <li><i class='bx bxl-github text-3xl text-lime-500'></i></li>
        </ul>
      </nav>

      <div class="flex gap-4">
        <div class="mt-7">
          <span class="leading-none border-lime-500 border-4 text-4xl font-semibold text-lime-500 p-2">LY</span>
        </div>

        <div>
          <h1 class="text-5xl mb-3">Lorem Ypsun</h1>
          <p class="text-xl font-light italic mb-2">Front Developer Youtuber Writer</p>
          <p class="text-xl font-light italic mb-3">HTML | CSS | Javascript | Vue |
            Writings | Lifestyle</p>

          <!-- <ul class="flex justify-end items-center gap-2">
            <li>
              <a href="www.github.com" target="_blank" rel="noopener noreferrer"><i
                  class='bx bxl-github text-3xl text-lime-500'></i></a>
            </li>
            <li>
              <a href="www.youtube.com" target="_blank" rel="noopener noreferrer"><i
                  class='bx bxl-youtube text-3xl text-lime-500'></i></a>
            </li>
          </ul> -->
        </div>
      </div>
    </header>

    <div class="flex justify-center my-8">
      <Separator class="bg-zinc-300 max-w-lg opacity-65" />
    </div>

    <!-- Pega os arquivos da pasta Page -->
    <NuxtPage />
  </div>
</template>

<style>
body {
  @apply bg-zinc-800 text-zinc-300
}

.container {
  @apply mx-auto max-w-5xl px-10
}
</style>