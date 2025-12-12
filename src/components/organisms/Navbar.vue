<template>
    <nav class="navbar-glass hide-on-idle">
  <router-link to="/" class="nav-item">
    <i class="pi pi-user"></i>
  </router-link>

  <router-link to="/projects" class="nav-item">
    <i class="pi pi-folder"></i>
  </router-link>

  <router-link to="/about" class="nav-item">
    <i class="pi pi-briefcase"></i>
  </router-link>
</nav>
</template>
<style>
.navbar-glass {
  position: fixed;
  top: 0px;
  left: 50%;
  transform: translateX(-50%);
  padding: 10px 25px;
  display: flex;
  gap: 25px;

  background: rgba(255, 255, 255, 0.05);
  border-radius: 0 0 20px 20px;
  backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);

  z-index: 1000;
  transition: transform 0.35s ease, opacity 0.25s ease;
}

.hide-on-idle {
  transform: translate(-50%, -80%);
  opacity: 0.4;
}

.navbar-glass:hover {
  transform: translate(-50%, 0);
  opacity: 1;
}

.nav-item {
  color: #c0c0c0;
  font-size: 1.9rem;
  padding: 8px 12px;
  border-radius: 14px;
  transition: 0.3s;
}

.nav-item:hover {
  color: #d4bcff;
  background: rgba(180, 100, 255, 0.12);
}

.nav-item.router-link-exact-active {
  color: #cba3ff;
  background: rgba(180, 100, 255, 0.25);
  box-shadow: 0 0 12px rgba(180, 100, 255, 0.4);
  transform: scale(1.15);
}

</style>

