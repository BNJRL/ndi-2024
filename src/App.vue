<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header class="ocean-header">
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <nav class="ocean-nav">
        <RouterLink class="nav-link" to="/">Home</RouterLink>
        <RouterLink class="nav-link" to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <main class="ocean-main">
    <RouterView />
  </main>
</template>

<style scoped>
/* Style général */
body {
  margin: 0;
  font-family: 'Arial', sans-serif;
  color: #fff;
  background: linear-gradient(to bottom, #005c97, #363795); /* Océan bleu et violet */
}

/* Header */
.ocean-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 2rem;
  background: rgba(0, 92, 151, 0.8);
  border-bottom: 2px solid #00aaff;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
}

.logo {
  animation: float 4s ease-in-out infinite;
}

/* Nav */
.ocean-nav {
  display: flex;
  gap: 1rem;
}

.nav-link {
  text-decoration: none;
  font-size: 1.2rem;
  color: #ffffff;
  padding: 0.5rem 1rem;
  border-radius: 8px;
  background: rgba(255, 255, 255, 0.2);
  transition: background 0.3s, transform 0.3s;
}

.nav-link:hover {
  background: rgba(255, 255, 255, 0.4);
  transform: translateY(-2px);
}

/* Main */
.ocean-main {
  padding: 2rem;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  backdrop-filter: blur(8px);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  margin: 2rem auto;
  max-width: 800px;
}

/* Animations */
@keyframes float {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}
</style>
