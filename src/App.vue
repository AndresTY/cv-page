<template>
  <navbar/>
  <router-view />
</template>

<script lang="ts">
import {computed, reactive} from 'vue';
import {useHead} from '@vueuse/head';
import Navbar from '@/components/organisms/Navbar.vue';

export default {
  components:{
    Navbar,
  },
  setup() {
    const siteData = reactive({
      title: 'Andres Ducuara',
      description: 'Curriculum Vitae Andres Santiago Ducuara Velasquez',
      link: [
        { rel: 'icon', href: require('@/assets/logo.png') }
      ]
    });


    useHead({
      link: computed(() => siteData.link),
      title: computed(() => siteData.title),
      meta: [
        {
          name: 'description',
          content: computed(() => siteData.description),
        },
      ],
    });
  },
};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  background-color: #000000;
  height: 100%;
  margin: 0; 
}

</style>
