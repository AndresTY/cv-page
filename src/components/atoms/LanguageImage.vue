<template>
  <div class="image-wrapper">
    <img loading="lazy" :src="src" :alt="alt" class="language-image">
  </div>
</template>

<script setup lang="ts">
defineProps({
  src: String,
  alt: String
})
</script>
