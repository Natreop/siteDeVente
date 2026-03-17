<template>
  <div class="home">
    <section class="hero">
      <h1>Bienvenue à Bavière Excursions</h1>
      <p>Explorez les merveilles de la Bavière avec nos excursions guidées</p>
    </section>

    <section class="introduction">
      <h2>Nos Meilleures Excursions</h2>
      <ProductList />
    </section>

    <section class="about">
      <About />
    </section>
  </div>
</template>

<script setup>
import About from '../components/About.vue'
import ProductList from '../components/ProductList.vue'
</script>

<style scoped>
.home {
  width: 100%;
}

.hero {
  background: linear-gradient(rgba(139, 69, 19, 0.8), rgba(139, 69, 19, 0.8)),
    url('https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=1200&h=400&fit=crop');
  background-size: cover;
  background-position: center;
  color: white;
  text-align: center;
  padding: 60px 20px;
}

.hero h1 {
  font-size: 3em;
  margin: 0;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.hero p {
  font-size: 1.3em;
  margin: 10px 0 0 0;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

.introduction,
.about {
  padding: 40px 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.introduction {
  background-color: #f5f1e8;
  text-align: center;
}

.introduction h2 {
  color: #8B4513;
  font-size: 2em;
  margin-bottom: 20px;
}

.about {
  background-color: white;
}
</style>