<script setup lang="ts">
const props = defineProps<{
    text: string,
    bgHover: string,
    textColor: string
}>();
</script>

<template>
  <button :class="`bg-red-600 ${textColor} py-1 z-10`">
    『<span class="font-spacing ml-3">{{ text }}</span>』
    <slot></slot>
  </button>
</template>