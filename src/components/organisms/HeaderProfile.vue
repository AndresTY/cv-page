<template>
    <section id="header" class="Page-content header">
      <div class="Page-content">
        <div class="bulbasaur">
          <div class="chikorita">
            <div class="music-bg bg bg-shadow-top">
              <div>
                <div class="image-container">
                    <img loading="lazy" :src="require('@/assets/images/music/man.png')" alt="Ducuara" class="img-fluid" />
                    </div>
                    <SocialNetworks />
                </div>
            </div>
          </div>
          <div class="chikorita">
            <div class="title title4 overlay-box objetc-list" style="pointer-events: none">
              <div class="nine">
                <h1>Andres Ducuara</h1>
                <h5>AI & Computer Science Engineer · M.Sc in Artificial Intelligence</h5>
                <h1><span><i class="pi pi-spin pi-microchip"></i></span></h1>
              </div>
            </div>
            <div class="objetc-list overlay-box text-center" style="pointer-events: none">
              <div>
                <h3>
                  Developer and researcher focused on the convergence of computer science and electronics to build intelligent and innovative solutions. Experienced in artificial intelligence, machine learning, cybersecurity, optimization, data analysis, and IoT.
                </h3>
              </div>
            </div>
            <br>
             <ButtonPrimary icon="btn btn-default back-white" 
             @click="$emit('download')">
                Download CV
            </ButtonPrimary>
          </div>
        </div>
      </div>
    </section>
</template>

<script setup>
import SocialNetworks from "@/components/molecules/SocialNetworks.vue";
import ButtonPrimary from "@/components/atoms/ButtonPrimary.vue";

</script>
<style>
    .chikorita{
        display:block; margin-left: auto; margin-right: auto; margin-top: auto; margin-bottom: auto
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

header .navbar {
  background-color: #343a40;
}

header .navbar .form-inline a {
  color: white;
}

header .navbar .form-inline i {
  font-size: 24px;
  margin-right: 10px;
  margin-left: 10px;
}

header .navbar .form-inline {
  padding-left: 10%;
  display: inline;
}
#header.Page-content.header {
  padding: 50px 0;
  background-image:linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), url('@/assets/images/backgrounds/main3.webp');
  background-size: cover;
}
.Page-content .bulbasaur {
  display: grid;
  grid-template-columns: 1fr 1fr; 
  margin: 0 auto;
  max-width: 2000px;
  gap: 1rem;
}
.Page-content .bulbasaur .chikorita {
  display: block;
  margin:auto;
}

.Page-content .bulbasaur .chikorita .music-bg {
  background-attachment: fixed;
}

.Page-content .bulbasaur .chikorita .music-bg .img-fluid {
  max-width: 80%;
  height: auto;
  transform-style: preserve-3d;
  transition: transform 0.3s ease-in-out;
}
.Page-content .bulbasaur .chikorita .music-bg .img-fluid:hover {
  transform: rotateY(15deg) rotateX(-15deg);
}

.Page-content .bulbasaur .chikorita .title4.overlay-box {
  text-align: center;
  color: #ffffff;
}

.Page-content .bulbasaur .chikorita .title4 h2 {
  font-size: 36px;
  font-weight: bold;
  margin-bottom: 10px;
}

.Page-content .bulbasaur .chikorita .title4 p {
  font-size: 16px;
  color: #fafafa;
  margin-bottom: 20px;
}

.Page-content .bulbasaur .chikorita .objetc-list.overlay-box {
  text-align: center;
  margin-top: 20px;
}

.Page-content .bulbasaur .chikorita .objetc-list h5 {
  font-size: 18px;
  color: #fafafa;
  line-height: 1.6;
  max-width: 800px;
  margin: 0 auto;
}
.Page-content .bulbasaur .chikorita .objetc-list h3 {
  font-size: 20px;
  color: #fafafa;
  line-height: 1.6;
  max-width: 800px;
  margin: 0 auto;
}

.Page-content .bulbasaur .chikorita .btn {
  font-size: 16px;
  background-color: #7700ff;
  color: white;
  padding: 10px 20px;
  border-radius: 5px;
  text-decoration: none;
  display: inline-block;
  transition: background-color 0.3s ease;
}

.Page-content .bulbasaur .chikorita .btn:hover {
  background-color: #490497;
}

.Page-content .bulbasaur .chikorita .music-bg.bg-shadow-top {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.3);
}

[data-tilt] {
  transform-style: preserve-3d;
  transition: transform 0.3s ease-in-out;
}

[data-tilt]:hover {
  transform: rotateY(5deg) rotateX(-5deg);
}

</style>