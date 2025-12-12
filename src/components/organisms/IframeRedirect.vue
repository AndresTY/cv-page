<template>
  <div>
    <iframe 
      :src="iframeSrc" 
      id="webpack-dev-server-client-overlay" >
    </iframe>

    <div id="webpack-dev-server-client-overlay-div">
      <div class="background-image"></div>
      <div class="popup">
        <h2>Site Under Maintenance!</h2>
        <p>We are working to improve the experience. The site will be up and running again very soon. Thank you for your patience!</p>
      </div>
    </div>

      <router-link to="/" class="redirect-button">
        <i class="pi pi-arrow-left"></i>
      </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      iframeSrc: 'about:blank',
    };
  },
};
</script>

<style scoped>
iframe{
  position: fixed; 
  inset: 0px; 
  width: 100vw; 
  height: 100vh; 
  border: none; 
  z-index: 2147483647;
  pointer-events: none;
}
.redirect-button {
  padding: 10px 20px;
  background-color: #00000010;
  color: white;
  border: none;
  cursor: pointer;
  text-decoration: none;
  position: fixed; 
  top: 10px;
  left: 10px;
  z-index: 1000; 
}
#webpack-dev-server-client-overlay-div {
  position: fixed;
  box-sizing: border-box;
  inset: 0px;
  width: 100vw;
  height: 100vh;
  font-size: large;
  padding: 2rem 2rem 4rem;
  line-height: 1.2;
  white-space: pre-wrap;
  overflow: auto;
  background-color: rgba(0, 0, 0, 0.9);
  color: white;
  z-index: 10;
}


#webpack-dev-server-client-overlay-div .popup {
  position: fixed; 
  top: 50%; 
  left: 50%; 
  transform: translate(-50%, -50%); 
  background-color: rgba(0, 0, 0, 0.7); 
  color: white; 
  padding: 20px; 
  border-radius: 10px; 
  z-index: 9999; 
  width: 80%; 
  max-width: 400px; 
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5); 
}
#webpack-dev-server-client-overlay-div .background-image {
  position: absolute; 
  inset: 0px;
  background-image: url('@/assets/images/backgrounds/obras.png'); 
  background-size: cover;
  background-position: center center;
  opacity: 0.2; 
  z-index: -1; 
}
</style>
