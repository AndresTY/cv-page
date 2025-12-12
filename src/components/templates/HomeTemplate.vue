<template>
  <div class="home-template">
    <Loader v-if="isLoading" />

    <HeaderProfile @download="downloadPDF" />

    <LanguageGrid :languages="languages" />

    <Footer />
  </div>
</template>

<script>
import Loader from '@/components/organisms/Loader.vue';
import HeaderProfile from '@/components/organisms/HeaderProfile.vue';
import LanguageGrid from '@/components/organisms/LanguageGrid.vue';
import Footer from '@/components/organisms/Footer.vue';

export default {
  name: "HomeTemplate",

  components: {
    Loader,
    HeaderProfile,
    LanguageGrid,
    Footer,
  },

  props: {
    isLoading: Boolean,
    languages: Array,
  },

  methods: {
    downloadPDF() {
      this.$emit("download");
    }
  }
};
</script>

<style scoped>
.home-template {
  padding: 20px;
}
</style>
