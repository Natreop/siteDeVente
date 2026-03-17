<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-section">
        <h4>Bavière Excursions</h4>
        <p>123 Rue des Excursions<br />
          63260 Thuret, France<br />
          Tel: +33 3 89 67 67 67<br />
          Email: contact@baviere-excursions.fr
        </p>
      </div>
      <div class="footer-section">
        <h4>Navigation</h4>
        <ul>
          <li><router-link to="/">Accueil</router-link></li>
          <li><router-link to="/products">Nos Excursions</router-link></li>
        </ul>
      </div>
      <div class="footer-section">
        <h4>Informations Légales</h4>
        <ul>
          <li><a href="#conditions">Conditions d'utilisation</a></li>
          <li><a href="#mentions">Mentions légales</a></li>
          <li><a href="#confidentialite">Politique de confidentialité</a></li>
        </ul>
      </div>
      <div class="footer-section">
        <h4>Suivez-nous</h4>
        <p>
          <a href="#facebook">Facebook</a> | 
          <a href="#instagram">Instagram</a> | 
          <a href="#twitter">Twitter</a>
        </p>
      </div>
    </div>
    <div class="footer-bottom">
      <p>© 2026 Bavière Excursions - Tous droits réservés</p>
      <p style="font-size: 0.9em; margin-top: 5px;">
        Conditions d'utilisation | Mentions légales | Politique de confidentialité
      </p>
    </div>
  </footer>
</template>

<script setup>
import { useRouter } from 'vue-router'
const router = useRouter()
</script>

<style scoped>
.footer {
  background: linear-gradient(135deg, #6B3410 0%, #8B4513 100%);
  color: white;
  padding: 40px 20px 20px;
  margin-top: auto;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto 30px;
  padding-bottom: 30px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.2);
}

.footer-section h4 {
  margin: 0 0 15px 0;
  font-size: 1.1em;
  color: #FFD700;
}

.footer-section p {
  margin: 0;
  line-height: 1.6;
}

.footer-section ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-section li {
  margin-bottom: 5px;
}

.footer-section a {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s;
}

.footer-section a:hover {
  color: #FFD700;
}

.footer-bottom {
  text-align: center;
  font-size: 0.9em;
  opacity: 0.9;
}

.footer-bottom p {
  margin: 0;
}
</style>