<template>
  <div 
    class="language-item"
    @mouseover="isHovered = true"
    @mouseleave="isHovered = false"
  >
    <LanguageImage :src="imageUrl" :alt="text" />

    <ProgressBar :progress="progress" />

    <HoverText v-if="isHovered">
      {{ text }}
    </HoverText>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import LanguageImage from "@/components/atoms/LanguageImage.vue";
import ProgressBar from "@/components/atoms/ProgressBar.vue";
import HoverText from "@/components/atoms/HoverText.vue";

defineProps({
  imageUrl: String,
  progress: Number,
  text: String
});

const isHovered = ref(false);
</script>
