<template>
  <div class="project-list">
    <div class="nine">
                <h1>Main Projects</h1>
                <h1><span><i class="pi pi-spin pi-microchip"></i></span></h1>
              </div>
    <ProjectCard
      v-for="(p, i) in projects"
      :key="i"
      :image="p.image"
      :title="p.title"
      :description="p.description"
      :skills="p.skills"
      :github="p.github"
    />
  </div>
</template>

<script setup>
import ProjectCard from "@/components/molecules/ProjectCard.vue";

defineProps({
    projects: Array
});

</script>

<style scoped>
.project-list {
  display: grid;
  gap: 30px;
  padding: 20px;
}
    .nine h1 {
  text-align:center; font-size:50px; text-transform:uppercase; color:#ffffff; letter-spacing:1px;
  font-family:"Playfair Display", serif; font-weight:400;
}
.nine h1 span {
  margin-top: 5px;
    font-size:15px; color:#ffffff; word-spacing:1px; font-weight:normal; letter-spacing:2px;
    text-transform: uppercase; font-family:"Playfair Display", sans-serif; font-weight:500;

    display: grid;
    grid-template-columns: 1fr max-content 1fr;
    grid-template-rows: 27px 0;
    grid-gap: 20px;
    align-items: center;
}

.nine h1 span:after,.nine h1 span:before {
    content: " ";
    display: block;
    border-bottom: 1px solid #ccc;
    border-top: 1px solid #ccc;
    height: 5px;
  background-color:#f8f8f8;
}
</style>
