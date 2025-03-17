<template>
  <main class="main">
    <div class="content">
      <h2>Prêt pour un Blind Test musical ?</h2>
      <p>Affrontez vos amis et testez vos connaissances en musique.</p>
      <button>Jouer maintenant</button>
    </div>
  </main>
</template>

<style scoped>
/* Assurer que tout l'écran est occupé */
.main {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100vw;
  height: 100vh;
  background: linear-gradient(135deg, #007bff, #6610f2);
  color: white;
  text-align: center;
  padding: 20px;
  box-sizing: border-box; /* Évite tout débordement */
}

.content {
  max-width: 600px;
}

h2 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

p {
  font-size: 1.2rem;
  margin-bottom: 20px;
}

button {
  background-color: #ffcc00;
  color: #333;
  font-size: 1.2rem;
  font-weight: bold;
  padding: 12px 20px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: transform 0.2s ease, background-color 0.3s ease;
}

button:hover {
  background-color: #ffdb4d;
  transform: scale(1.05);
}

@media screen and (max-width: 768px) {
  h2 {
    font-size: 2rem;
  }

  p {
    font-size: 1rem;
  }

  button {
    font-size: 1rem;
    padding: 10px 15px;
  }
}
</style>

<style>
/* Réinitialisation des marges et paddings globaux */
html, body {
  margin: 0;
  padding: 0;
  width: 100vw;
  height: 100vh;
  overflow: hidden; /* Empêche le défilement */
}
</style>