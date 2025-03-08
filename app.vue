<template>
  <div class="max-w-3xl px-4 mx-auto">
    <header class="mt-8 mb-4 flex justify-between items-end">
      <div>
        <h1 class="text-2xl font-semibold">Personal Blog</h1>
        <p class="text-gray-500">learning programming</p>
      </div>

      <!-- <Btn>Hire Me</Btn>   -->
    </header>

    <!-- Pega os arquivos da pasta Page -->
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
    <!-- <NuxtRouteAnnouncer />
    <NuxtWelcome /> -->
  </div>
</template>

<style>
  body {
    @apply bg-gray-500
  }
</style>