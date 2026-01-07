<script setup lang="ts"></script>

<template>
  <div class="maintenance-container">
    <div class="content">
      <div class="logo-wrapper">
        <svg viewBox="0 0 24 24" class="spotify-logo" xmlns="http://www.w3.org/2000/svg">
          <path d="M12 0C5.4 0 0 5.4 0 12s5.4 12 12 12 12-5.4 12-12S18.66 0 12 0zm5.521 17.34c-.24.359-.66.48-1.021.24-2.82-1.74-6.36-2.101-10.561-1.141-.418.122-.779-.179-.899-.539-.12-.421.18-.78.54-.9 4.56-1.021 8.52-.6 11.64 1.32.42.18.479.659.301 1.02zm1.44-3.3c-.301.42-.841.6-1.262.3-3.239-1.98-8.159-2.58-11.939-1.38-.479.12-1.02-.12-1.14-.6-.12-.48.12-1.021.6-1.141C9.6 9.9 15 10.561 18.72 12.84c.361.181.54.78.241 1.2zm.12-3.36C15.24 8.4 8.82 8.16 5.16 9.301c-.6.179-1.2-.181-1.38-.721-.18-.601.18-1.2.72-1.381 4.26-1.26 11.28-1.02 15.721 1.621.539.3.719 1.02.419 1.56-.299.421-1.02.599-1.559.3z" fill="#FFF"/>
        </svg>
      </div>
      <h1 class="title">Application en développement</h1>
    </div>
  </div>
</template>

<style scoped>
.maintenance-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
  background-color: #000000;
  color: white;
  font-family: 'Circular Std', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  overflow: hidden;
  position: fixed;
  top: 0;
  left: 0;
}

.content {
  text-align: center;
  z-index: 10;
}

.logo-wrapper {
  margin-bottom: 2rem;
  animation: float 6s ease-in-out infinite;
}

.spotify-logo {
  width: 120px;
  height: 120px;
  filter: drop-shadow(0 0 20px rgba(29, 185, 84, 0.6));
  transition: filter 0.3s ease;
}

.title {
  font-size: 2rem;
  font-weight: 700;
  letter-spacing: -0.5px;
  animation: fadeIn 2s ease-out;
  color: #FFFFFF;
  text-shadow: 0 4px 12px rgba(0,0,0,0.5);
}

@keyframes float {
  0% {
    transform: translateY(0px) rotate(0deg);
  }
  50% {
    transform: translateY(-20px) rotate(1deg);
    filter: drop-shadow(0 0 35px rgba(29, 185, 84, 0.8));
  }
  100% {
    transform: translateY(0px) rotate(0deg);
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 600px) {
  .spotify-logo {
    width: 80px;
    height: 80px;
  }
  .title {
    font-size: 1.5rem;
  }
}
</style>
