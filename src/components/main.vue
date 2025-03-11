<template>
  
    <nav class="navbar">
      <h1>Bienvenue sur notre site de blind test</h1>
    </nav>
  </template>
  
  <style scoped>
  .navbar {
    display: flex;
    justify-content: center;
    gap: 20px;
    padding: 12px 20px;
    background-color: #4a4a4a;
    border-bottom: 3px solid #333;
  }
  
  .navbar a {
    text-decoration: none;
    color: white;
    font-weight: bold;
    padding: 8px 12px;
    border-radius: 5px;
    transition: background-color 0.3s ease-in-out, color 0.3s ease-in-out;
  }

  .navbar a:hover {
    background-color: #ffffff;
    color: #4a4a4a;
  }
  
  .navbar a.router-link-active {
    text-decoration: underline;
    color: #ffcc00;
  }

  .main {
    background-color: #007bff;
    color: white;
    padding: 20px;
    min-height: 80vh;
  }
</style>