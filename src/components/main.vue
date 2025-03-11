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
    padding: 10px;
    background-color: grey;
  }
  
  .navbar a {
    text-decoration: none;
    color: black;
    font-weight: bold;
  }
  
  .navbar a.router-link-active {
    text-decoration: underline;
  }

  .main{
    background-color: blue;
  }
  </style>