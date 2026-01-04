<script setup>
</script>

<template>
  <div class="home-container">
    <div class="hero">
      <h1>Choisissez votre examen</h1>
      <p>Sélectionnez une catégorie pour commencer le QCM</p>
    </div>

    <div class="info-section">
      <h3>⚠️ Informations Importantes</h3>
      <p>
        Attention, ce ne sont pas tout le temps juste des QCM.
        <br>
        J'ai fait au mieux pour réaliser ce projet.
      </p>
    </div>

    <div class="grid-container">
      
      <!-- XML Card -->
      <a href="https://xml.up.railway.app/" target="_blank" class="card xml-card">
        <div class="card-content">
          <div class="icon-wrapper">
            <span class="icon">&lt;/&gt;</span>
          </div>
          <h2>QCM XML</h2>
          <p>Testez vos connaissances en balisage</p>
        </div>
        <div class="card-bg"></div>
      </a>

      <!-- DASC Card -->
      <a href="https://dasc.up.railway.app/" target="_blank" class="card dasc-card">
        <div class="card-content">
          <div class="icon-wrapper">
            <span class="icon">☁️</span>
          </div>
          <h2>QCM DASC</h2>
          <p>Distributed Application Service Component</p>
        </div>
        <div class="card-bg"></div>
      </a>

      <!-- Kotlin Card -->
      <a href="https://kotlin.up.railway.app/" target="_blank" class="card kotlin-card">
        <div class="card-content">
          <div class="icon-wrapper">
            <span class="icon">K</span>
          </div>
          <h2>QCM Kotlin</h2>
          <p>Le langage moderne pour Android</p>
        </div>
        <div class="card-bg"></div>
      </a>

      <!-- C# Card -->
      <a href="https://csharp.up.railway.app/" target="_blank" class="card csharp-card">
        <div class="card-content">
          <div class="icon-wrapper">
            <span class="icon">C#</span>
          </div>
          <h2>QCM C#</h2>
          <p>Maîtrisez le framework .NET</p>
        </div>
        <div class="card-bg"></div>
      </a>

    </div>
  </div>
</template>

<style scoped>
.home-container {
  width: 100%;
  padding: 2rem;
  box-sizing: border-box;
}

.hero {
  margin-bottom: 4rem;
  text-align: center;
}

.hero h1 {
  font-size: 3rem;
  margin-bottom: 0.5rem;
  background: linear-gradient(to right, #fff, #a5a5a5);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.hero p {
  color: #8b8b9b;
  font-size: 1.2rem;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.card {
  position: relative;
  height: 300px;
  background: rgba(255, 255, 255, 0.03);
  border-radius: 20px;
  text-decoration: none;
  overflow: hidden;
  border: 1px solid rgba(255, 255, 255, 0.05);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 2rem;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
  border-color: rgba(255, 255, 255, 0.2);
}

.card-content {
  z-index: 2;
  position: relative;
}

.icon-wrapper {
  background: rgba(255, 255, 255, 0.1);
  width: 60px;
  height: 60px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
  backdrop-filter: blur(5px);
  box-shadow: 0 4px 15px rgba(0,0,0,0.2);
}

.icon {
  font-size: 1.5rem;
  font-weight: bold;
  color: #fff;
}

.card h2 {
  color: #fff;
  margin: 0 0 0.5rem 0;
  font-size: 1.5rem;
}

.card p {
  color: #a0a0b0;
  margin: 0;
  font-size: 0.9rem;
}

/* Specific Card Styles (Gradients) */
.xml-card .card-bg {
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  background: radial-gradient(circle at top right, rgba(255, 107, 107, 0.15), transparent 60%);
  transition: opacity 0.3s;
}

.dasc-card .card-bg {
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  background: radial-gradient(circle at top right, rgba(78, 205, 196, 0.15), transparent 60%);
}

.kotlin-card .card-bg {
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  background: radial-gradient(circle at top right, rgba(162, 155, 254, 0.15), transparent 60%);
}

.csharp-card .card-bg {
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  background: radial-gradient(circle at top right, rgba(108, 92, 231, 0.2), transparent 60%);
}

.card:hover .card-bg {
  filter: brightness(1.2);
}

.info-section {
  margin-bottom: 3rem;
  padding: 2rem;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 12px;
  border-left: 5px solid #ffcc00;
  backdrop-filter: blur(5px);
  text-align: center;
}

.info-section h3 {
  margin-top: 0;
  color: #ffcc00;
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.info-section p {
  color: #ddd;
  font-size: 1.1rem;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .home-container {
    padding: 1rem;
  }

  .hero {
    margin-bottom: 2.5rem;
  }

  .hero h1 {
    font-size: 2.2rem;
  }
  
  .hero p {
    font-size: 1rem;
  }

  .info-section {
    padding: 1.5rem;
    margin-bottom: 2rem;
  }

  .info-section h3 {
    font-size: 1.3rem;
  }

  .info-section p {
    font-size: 1rem;
  }

  .grid-container {
    gap: 1.5rem;
    grid-template-columns: 1fr; /* Force single column on mobile for better focus */
  }

  .card {
    height: 250px; /* Slightly shorter on mobile */
  }
}
</style>
