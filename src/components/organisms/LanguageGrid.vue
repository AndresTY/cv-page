<template>
  <section id="language" class="section-language">
    <h1 class="main-title">Languages</h1>

    <div class="language-container">
      <LanguageItem
        v-for="(lang, i) in languages"
        :key="i"
        :imageUrl="lang.imageUrl"
        :text="lang.text"
        :progress="lang.progress"
      />
    </div>
  </section>
</template>

<script setup>
import LanguageItem from "@/components/molecules/LanguageItem.vue";

defineProps({
  languages: Array
});
</script>

<style>
    language.section-language{
  background-image:linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)),url('@/assets/images/backgrounds/language-bg.png');
  background-size:cover;
}
.section-language h1{
  ext-align:center; font-size:50px; text-transform:uppercase; color:#ffffff; letter-spacing:1px;
  font-family:"Playfair Display", serif; font-weight:400;
}

.language-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  padding: 20px;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  box-sizing: border-box;
}

.language-item {
  position: relative;
  overflow: hidden;
  aspect-ratio: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border-radius: 8px;
  padding: 10px;
  min-height: 200px;
}

.image-wrapper {
  width: 100%;
  height: calc(100% - 30px);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.3s ease;
}

.language-image {
  width: 70%;
  height: 70%;
  object-fit: contain;
  transition: all 0.3s ease;
}

.language-item:hover .image-wrapper {
  transform: scale(1.2);
  z-index: 2;
}

.language-item:hover .language-image {
  width: 90%;
  height: 90%;
}

.progress-container {
  width: 100%;
  height: 20px;
  background-color: #e0e0e0;
  border-radius: 10px;
  overflow: hidden;
  margin-top: auto;
  position: relative;
  z-index: 1;
}

.progress-bar {
  height: 100%;
  background: linear-gradient(90deg, #7704f9, #7700ff);
  transition: width 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
}

.progress-text {
  color: white;
  font-size: 0.8em;
  font-weight: bold;
  text-shadow: 1px 1px 1px rgba(0,0,0,0.2);
}

.hover-text {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.8);
  color: white;
  padding: 10px;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.1em;
  z-index: 3;
  opacity: 0;
  animation: fadeIn 0.3s ease forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@media screen and (max-width: 768px) {
  .language-container {
    grid-template-columns: repeat(2, 1fr);
    padding: 15px;
  }
  
  .language-item {
    min-height: 180px;
  }
  
  .progress-text {
    font-size: 0.7em;
  }
}

@media screen and (max-width: 480px) {
  .language-container {
    grid-template-columns: 1fr;
    padding: 10px;
  }
  
  .language-item {
    min-height: 160px;
  }
}

/* Ajustes para pantallas muy grandes */
@media screen and (min-width: 1400px) {
  .language-container {
    max-width: 1400px;
  }
}
</style>