<template>
  <header class="header">
    <nav class="navbar">
      <h1>Bienvenue sur notre site de Blind Test</h1>
      <div class="nav-links">
        <a href="#">Accueil</a>
        <a href="#">Jouer</a>
        <a href="#">Classement</a>
        <a href="#">Contact</a>
      </div>
    </nav>
  </header>
</template>

<style scoped>
/* Barre de navigation */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 15px 30px;
  background: linear-gradient(135deg, #1e3c72, #2a5298);
  color: white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
}

.navbar h1 {
  font-size: 1.8rem;
  margin: 0;
  text-align: left;
}

/* Liens de navigation */
.nav-links {
  display: flex;
  gap: 15px;
}

.nav-links a {
  text-decoration: none;
  color: white;
  font-weight: bold;
  padding: 8px 15px;
  border-radius: 8px;
  transition: background-color 0.3s ease, color 0.3s ease;
}

.nav-links a:hover,
.nav-links a:focus {
  background-color: rgba(255, 255, 255, 0.3);
}

/* Responsive */
@media screen and (max-width: 768px) {
  .navbar {
    flex-direction: column;
    text-align: center;
    padding: 15px;
  }

  .nav-links {
    flex-direction: column;
    gap: 10px;
    align-items: center;
  }
}
</style>