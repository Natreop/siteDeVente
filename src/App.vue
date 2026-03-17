<script setup>
import { useRouter } from 'vue-router'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

const router = useRouter()
</script>

<template>
  <div id="app">
    <Header />
    <nav class="navbar">
      <router-link to="/" class="nav-link">Accueil</router-link>
      <router-link to="/products" class="nav-link">Nos Excursions</router-link>
    </nav>
    <main class="main-content">
      <router-view />
    </main>
    <Footer />
  </div>
</template>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.navbar {
  background-color: #6B4423;
  padding: 15px;
  display: flex;
  gap: 20px;
  justify-content: center;
  border-bottom: 2px solid #8B4513;
}

.nav-link {
  color: white;
  text-decoration: none;
  font-weight: bold;
  padding: 8px 15px;
  border-radius: 4px;
  transition: background-color 0.3s;
}

.nav-link:hover {
  background-color: #8B4513;
}

.nav-link.router-link-active {
  background-color: #FFD700;
  color: #333;
}

.main-content {
  flex: 1;
  background-color: #f5f1e8;
}
</style>
