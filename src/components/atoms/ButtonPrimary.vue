<template>
  <button :class="icon" @click="$emit('click')">
    <slot />
  </button>
</template>
<script setup lang="ts">
    defineProps({
        icon:{type:String,default:"btn-primary"}
    })
</script>
