<template>
  <div class="container">
    <header>
      <nav class=" p-4">
        <ul class="flex justify-end">
          <li><i class='bx bx-search-alt-2 text-3xl text-lime-500'></i></li>
          <li>back</li>
        </ul>
      </nav>

      <div class="flex gap-4">
        <div class="mt-7">
          <span class="leading-none border-lime-500 border-4 text-4xl font-semibold text-lime-500 p-2">LY</span>
        </div>

        <div>
          <h1 class="text-5xl mb-3">Lorem Ypsun</h1>
          <p class="text-xl font-light italic mb-2">Front Developer Youtuber Writer</p>
          <p class="text-xl font-light italic mb-2">HTML | CSS | Javascript | Vue | 
            Writings | Lifestyle</p>

            <ul class="flex justify-end items-center gap-2">
              <li>
                <a href="www.github.com" target="_blank" rel="noopener noreferrer"><i class='bx bxl-github text-3xl text-lime-500' ></i></a>
              </li>
              <li>
                <a href="www.youtube.com" target="_blank" rel="noopener noreferrer"><i class='bx bxl-youtube text-3xl text-lime-500' ></i></a>
              </li>
            </ul>
        </div>
      </div>
    </header>

    <div>
    <Button>Click me</Button>
  </div>

    <!-- Pega os arquivos da pasta Page -->
    <<NuxtRouteAnnouncer />
    <NuxtPage />
  </div>
</template>

<style>
body {
  @apply bg-zinc-800 text-zinc-300

}
.container {
  /* também damos uma largura máxima de 1024px para a tela */
  @apply mx-auto max-w-5xl px-10
}
</style>