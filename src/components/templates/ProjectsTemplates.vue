<template>
  <div class="projects-template">
    <Loader v-if="isLoading" />
    <ProjectList :projects="projects"/>
    <Footer />
  </div>
</template>

<script>
import Loader from '@/components/organisms/Loader.vue';
import Footer from '@/components/organisms/Footer.vue';
import ProjectList from '@/components/organisms/ProjectList.vue';

export default {
  name: "ProjectsTemplate",

  components: {
    Loader,
    ProjectList,
    Footer,
  },

  props: {
    isLoading: Boolean,
    projects: Array,
  },

};
</script>

<style scoped>
.home-template {
  padding: 20px;
}
</style>
