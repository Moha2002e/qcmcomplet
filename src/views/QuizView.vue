<script setup>
import { useRoute } from 'vue-router';

// This is just a placeholder view to avoid 404s when clicking the cards
const route = useRoute();
const category = route.params.category;
</script>

<template>
  <div class="quiz-placeholder">
    <h1>QCM {{ category.toUpperCase() }}</h1>
    <p>Le contenu du QCM arrivera bientôt...</p>
    <router-link to="/" class="back-link">← Retour</router-link>
  </div>
</template>

<style scoped>
.quiz-placeholder {
  text-align: center;
  padding: 4rem;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 20px;
  backdrop-filter: blur(10px);
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

p {
  font-size: 1.2rem;
  color: #a0a0b0;
  margin-bottom: 2rem;
}

.back-link {
  display: inline-block;
  padding: 0.8rem 1.5rem;
  background: rgba(255, 255, 255, 0.1);
  color: #fff;
  text-decoration: none;
  border-radius: 8px;
  transition: background 0.3s;
}

.back-link:hover {
  background: rgba(255, 255, 255, 0.2);
}
</style>
