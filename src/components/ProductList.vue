<template>
  <section class="products">
    <div class="grid">
      <router-link v-for="product in products" :key="product.id" :to="'/products'" class="card">
        <div class="card-image">
          <img :src="product.image" :alt="product.name" />
        </div>
        <div class="card-content">
          <h3>{{ product.name }}</h3>
          <p class="location">📍 {{ product.location }}</p>
          <p class="price">À partir de {{ product.price }}€</p>
        </div>
      </router-link>
    </div>
  </section>
</template>

<script setup>
const products = [
  {
    id: 1,
    name: "Visite de Brasserie  Weihenstephan",
    location: "Colmar",
    image: "https://letempsdunebiere.ca/wp-content/uploads/2023/08/Brauerei_Weihenstephan-547990582-e1692535343618.jpg",
    price: 25
  },
  {
    id: 2,
    name: "Excursion en Montagne",
    location: "Kofel",
    image: "https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=250&h=350&fit=crop",
    price: 35
  },
  {
    id: 3,
    name: "Dégustation de Bière Locale",
    location: "Cologne",
    image: "https://images.unsplash.com/photo-1535958636474-b021ee887b13?w=250&h=350&fit=crop",
    price: 30
  },
  {
    id: 4,
    name: "Dégustation de Bière Locale",
    location: "Munich",
    image: "https://cdn.shopify.com/s/files/1/0242/4992/5687/files/image-investissez-tireuse.jpg?v=1693385906",
    price: 30
  }
]
</script>

<style scoped>
.products {
  padding: 20px 0;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 25px;
  padding: 0 20px;
}

.card {
  text-decoration: none;
  color: inherit;
  background: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}

.card-image {
  width: 100%;
  height: 300px;
  overflow: hidden;
  background-color: #f0f0f0;
}

.card-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card-content {
  padding: 15px;
}

.card-content h3 {
  margin: 0 0 8px 0;
  color: #8B4513;
  font-size: 1.1em;
}

.location {
  color: #999;
  font-size: 0.9em;
  margin: 0 0 10px 0;
}

.price {
  color: #FFD700;
  font-weight: bold;
  font-size: 1.1em;
  margin: 0;
}
</style>