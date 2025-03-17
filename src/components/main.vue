<template>
  <main class="main">
    <div class="content">
      <h2>Prêt pour un Blind Test musical ?</h2>
      <p>Affrontez vos amis et testez vos connaissances en musique.</p>
      <button @click="startGame" aria-label="Lancer le Blind Test">Jouer maintenant</button>
    </div>
  </main>
</template>

<script setup>
const startGame = () => {
  alert("Le jeu va commencer !");
};
</script>

<style scoped>
.main {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  width: 100%;
  background: linear-gradient(135deg, #007bff, #6610f2);
  color: white;
  text-align: center;
  box-sizing: border-box;
  overflow: hidden;
  padding: 20px;
}

.content {
  max-width: 600px;
  width: 90%;
}

h2 {
  font-size: 3rem;
  margin-bottom: 15px;
}

p {
  font-size: 1.5rem;
  margin-bottom: 25px;
}

button {
  background-color: #ffcc00;
  color: #333;
  font-size: 1.5rem;
  font-weight: bold;
  padding: 15px 25px;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  transition: transform 0.2s ease, background-color 0.3s ease;
}

button:hover {
  background-color: #ffdb4d;
  transform: scale(1.1);
}

@media screen and (max-width: 768px) {
  h2 {
    font-size: 2.2rem;
  }

  p {
    font-size: 1.2rem;
  }

  button {
    font-size: 1.2rem;
    padding: 12px 20px;
  }
}
</style>

<style>
/* Normalisation et suppression du scroll inutile */
html, body {
  margin: 0;
  padding: 0;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  font-family: Arial, sans-serif;
}
</style>