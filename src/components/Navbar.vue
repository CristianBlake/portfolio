<script setup lang="ts">
import { ref } from 'vue';

import Bars from '../components/Icons/Bars.vue';
import Close from '../components/Icons/Close.vue';
import Link from '../components/Link.vue';

const showLinks = ref(false);

const toggleShowLinks = () => {
  showLinks.value = !showLinks.value;
}
</script>

<template>
  <header>
    <nav class='relative'>
      <section class="p-2">
        <div class="bg-neutral-900 rounded-full flex items-center justify-between px-8 py-3">
          <a href='#'>
            <h1 class='self-center text-xl font-semibold whitespace-nowrap text-white'>Cristian J.</h1>
          </a>
  
          <button data-collapse-toggle='navbar-default' type='button'
            class='inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-white rounded-lg md:hidden'
            aria-controls='navbar-default' aria-expanded='false' @click="toggleShowLinks">
            <Bars />
          </button>
          <div class="hidden md:flex gap-8">
            <Link title='Home' link='#' />
            <Link title='Works' link='#' />
            <Link title='Contact' link='#' />
          </div>
        </div>

      </section>

      <Transition>
        <div class="md:hidden absolute top-0 w-screen h-screen bg-neutral-900" v-show="showLinks">
          <div class="relative h-full w-full flex flex-col items-center justify-center gap-8">
            <button class="absolute right-0 top-0 m-10 transition-all" @click="toggleShowLinks">
              <Close />
            </button>
  
            <Link title='Home' link='#' />
            <Link title='Works' link='#' />
            <Link title='Contact' link='#' />
          </div>
        </div>
      </Transition>
    </nav>
  </header>
</template>
