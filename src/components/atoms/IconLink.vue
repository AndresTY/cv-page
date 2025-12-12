<template>
  <a :href="href" target="_blank" class="icon-link">
    <i :class="icon" :style="{ fontSize: size, marginRight: right, marginLeft:left }"></i>
  </a>
</template>

<script setup lang="ts">
defineProps({
  href: String,
  icon: String,
  size: { type: String, default: "40px" },
  right: {type:String, default:"10px"},
  left: {type:String, default:"10px"}
})
</script>

<style scoped>
.icon-link {
  color: white;
  margin: 0 10px;
}
</style>
