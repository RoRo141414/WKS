<template>
    <nav class="navbar">
      <router-link to="/">Accueil</router-link>
      <router-link to="/categories">Catégories</router-link>
      <router-link to="/scores">Scores</router-link>
    </nav>
  </template>
  
  <style scoped>
  .navbar {
    display: flex;
    justify-content: center;
    gap: 20px;
    padding: 10px;
    background-color: #d9d9d9;
  }
  
  .navbar a {
    text-decoration: none;
    color: black;
    font-weight: bold;
  }
  
  .navbar a.router-link-active {
    text-decoration: underline;
  }
  </style>