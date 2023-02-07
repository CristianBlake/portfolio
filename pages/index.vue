<template>
  <main class="h-screen main-bg md:main-bg-lg">
    <section class="h-full grid grid-cols-1 justify-items-center content-center">
        <HomeTitle />
    </section>
    <Clouds />
  </main>
  <section>
    <h2>Trabajo</h2>
  </section>
</template>

<style scoped>
.main-bg {
  background: linear-gradient(180deg, rgba(12,74,110,1) 54%, rgba(255,255,255,1) 100%);
}

.main-bg-lg {
  background: #0c4a6e;
}
</style>