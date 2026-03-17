<template>
  <section class="about">
    <h2>Qui sommes-nous ?</h2>
    <div class="about-content">
      <p>
        <strong>Bavière Excursions</strong>
      </p>
      <p id="company-description">
        Texte à compléter plus tard...
      </p>
    </div>
  </section>
</template>

<script setup>
// This allows the admin to update the description later
const updateDescription = (text) => {
  const el = document.getElementById('company-description')
  if (el) el.textContent = text
}

defineExpose({ updateDescription })
</script>

<style scoped>
.about {
  padding: 40px 20px;
  background-color: #f9f5f0;
}

.about h2 {
  color: #8B4513;
  text-align: center;
  font-size: 2em;
  margin-bottom: 30px;
}

.about-content {
  max-width: 800px;
  margin: 0 auto;
}

.about-content p {
  color: #333;
  line-height: 1.8;
  margin: 0 0 20px 0;
  font-size: 1.05em;
}

.about-content p:last-child {
  margin-bottom: 0;
}

strong {
  color: #8B4513;
}
</style>