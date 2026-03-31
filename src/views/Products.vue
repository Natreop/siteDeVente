<template>
  <div class="products-page">
    <section class="products-header">
      <h1>Nos Excursions</h1>
      <p>Découvrez nos meilleures offres et réservez votre prochaine aventure</p>
    </section>

    <section class="products-grid">
      <div v-for="excursion in excursions" :key="excursion.id" class="excursion-card">
        <div class="excursion-image">
          <img :src="excursion.image" :alt="excursion.name" />
        </div>
        <div class="excursion-info">
          <h3>{{ excursion.name }}</h3>
          <p class="location">📍 {{ excursion.location }}</p>
          <p class="description">{{ excursion.description }}</p>
          <div class="details">
            <span class="duration">⏱️ {{ excursion.duration }}</span>
            <span class="difficulty">🏔️ {{ excursion.difficulty }}</span>
          </div>
          <p class="price">{{ excursion.price }}€ par personne</p>
          <button class="btn-order">Réserver Maintenant</button>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const excursions = [
  {
    id: 1,
    name: "Visite de Brasserie Weihenstephan",
    location: "Colmar",
    description: "Découvrez les secrets de la fabrication de la bière traditionnelle avec une visite guidée complète et une dégustation exclusive.",
    image: "https://letempsdunebiere.ca/wp-content/uploads/2023/08/Brauerei_Weihenstephan-547990582-e1692535343618.jpg",
    duration: "3 heures",
    difficulty: "Facile",
    price: 25
  },
  {
    id: 2,
    name: "Excursion en Montagne",
    location: "Kofel",
    description: "Une randonnée spectaculaire à travers les montagnes des Vosges avec vue panoramique sur la vallée de Ribeauvillé.",
    image: "https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=250&h=350&fit=crop",
    duration: "5 heures",
    difficulty: "Moyen",
    price: 35
  },
  {
    id: 3,
    name: "Dégustation de Bière Locale",
    location: "Cologne",
    description: "Une expérience gastronomique unique combinant visite historique et dégustation des meilleures bières locales alsaciennes.",
    image: "https://images.unsplash.com/photo-1535958636474-b021ee887b13?w=250&h=350&fit=crop",
    duration: "2.5 heures",
    difficulty: "Facile",
    price: 30
  },
  {
    id: 4,
    name: "Dégustation de Bière Locale",
    location: "Munich",
    description: "Parcourez les vignobles alsaciens en randonnée avec arrêts dans les caves et dégustations de vins reconnues internationalement.",
    image: "https://cdn.shopify.com/s/files/1/0242/4992/5687/files/image-investissez-tireuse.jpg?v=1693385906",
    duration: "4 heures",
    difficulty: "Facile",
    price: 30
  }
]
</script>

<style scoped>
.products-page {
  width: 100%;
}

.products-header {
  background: linear-gradient(rgba(139, 69, 19, 0.9), rgba(139, 69, 19, 0.9)),
    url('https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=1200&h=300&fit=crop');
  background-size: cover;
  background-position: center;
  color: white;
  text-align: center;
  padding: 40px 20px;
}

.products-header h1 {
  font-size: 2.5em;
  margin: 0;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.products-header p {
  font-size: 1.1em;
  margin: 10px 0 0 0;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 30px;
  padding: 40px 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.excursion-card {
  background: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.excursion-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
}

.excursion-image {
  width: 100%;
  height: 300px;
  overflow: hidden;
  background-color: #f0f0f0;
}

.excursion-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.excursion-info {
  padding: 20px;
}

.excursion-info h3 {
  margin: 0 0 8px 0;
  color: #8B4513;
  font-size: 1.3em;
}

.location {
  color: #999;
  font-weight: bold;
  margin: 0 0 10px 0;
  font-size: 0.95em;
}

.description {
  color: #555;
  margin: 0 0 15px 0;
  font-size: 0.95em;
  line-height: 1.4;
}

.details {
  display: flex;
  gap: 15px;
  margin: 15px 0;
  padding: 10px 0;
  border-top: 1px solid #eee;
  border-bottom: 1px solid #eee;
  font-size: 0.9em;
}

.duration,
.difficulty {
  flex: 1;
  color: #8B4513;
}

.price {
  font-size: 1.4em;
  font-weight: bold;
  color: #FFD700;
  margin: 15px 0;
}

.btn-order {
  width: 100%;
  padding: 10px;
  background-color: #8B4513;
  color: white;
  border: none;
  border-radius: 4px;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.3s;
}

.btn-order:hover {
  background-color: #6B3410;
}
</style>