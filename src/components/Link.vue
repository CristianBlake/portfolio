<script setup lang="ts">
const props = defineProps<{
    title: string,
    link: string
}>();

const { title, link } = props;
</script>

<template>
    <a class="text-white text-6xl md:text-xl font-bold" :href="link">{{ title }}</a>
</template>