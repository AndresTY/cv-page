<template>
  <div class="project-card">
    <div class="project-img">
      <img :src="resolveImg(image)" alt="Project image" />
    </div>

    <div class="project-info">
      
      <h2 class="title">{{ title }}</h2>
      <p class="description">{{ description }}</p>

      <ul class="skills">
        <li v-for="(skill, i) in skills" :key="i">{{ skill }}</li>
      </ul>

       <IconLink 
       :href="github"
       icon="pi pi-github"
       />

    </div>
  </div>
</template>

<script>

import IconLink from "@/components/atoms/IconLink.vue";
export default {
  name: "ProjectCard",
  components: {
    IconLink,
  },
  props: {
    image: { type: String, required: true },     
    title: { type: String, required: true },     
    description: { type: String, required: true },   
    skills: { type: Array, required: true },     
    github: { type: String, required: true },  
  },

  methods: {
    resolveImg(path) {
      try {
        return require(`@/assets/images/projects/${path}`);
      } catch {
        return require(`@/assets/images/logo/programing.png`); 
      }
    }
  }
};
</script>

<style scoped>
.project-card {
  display: grid;
  grid-template-columns: 250px 1fr;
  gap: 20px;

  width: 50%;             
  margin: 0 auto;        

  background: #0f0f0f;
  padding: 20px;
  border-radius: 12px;
  color: white;
  border: 1px solid #333;
}

.project-img img {
  width: 100%;
  height: auto;
  border-radius: 10px;
}

.project-info {
  display: flex;
  flex-direction: column;
  justify-content: center;  
  align-items: center;       
  text-align: center;        
  gap: 10px;                 
}

.title {
  font-size: 24px;
  margin: 0;
}

.description {
  opacity: 0.8;
  margin: 10px 0;
}

.skills {
  display: flex;            
  flex-wrap: wrap;          
  gap: 8px;                 
  padding: 0;
  margin: 10px 0;
  list-style: none;
}

.skills li {
  background: #1a1a1a;
  padding: 6px 12px;
  border-radius: 8px;       
  font-size: 14px;
  color: #cdbaff;
  border: 1px solid #333;
  white-space: nowrap;    
}
.github-link {
  margin-top: 10px;
  font-size: 35px;
  color: white;
  transition: 0.3s;
}

.github-link:hover {
  color: #8b4dff;
}

</style>
