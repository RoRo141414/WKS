<template>
    <main class="main">
      <div class="content">
        <h2>Prêt pour un Blind Test musical ?</h2>
        <p>Affrontez vos amis et testez vos connaissances en musique.</p>
      </div>
      
      <section class="categories">
        <h3>Choisissez une catégorie :</h3>
        <div class="category-list">
          <button 
            v-for="category in categories" 
            :key="category" 
            @click="$emit('select-category', category)" 
            class="category-button"
            :aria-label="'Choisir la catégorie ' + category"
          >
            {{ category }}
          </button>
        </div>
      </section>
    </main>
  </template>
  
  <script>
  export default {
    data() {
      return {
        categories: ['Années 80', 'Rock', 'Pop', 'Rap', 'Variété française']
      };
    }
  };
  </script>
  
  <style scoped>
  .main {
    display: flex;
    
    flex-direction: column;
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
    margin-bottom: 30px;
  }
  
  h2 {
    font-size: 3rem;
    margin-bottom: 15px;
  }
  
  p {
    font-size: 1.5rem;
    margin-bottom: 25px;
  }
  
  .categories {
    text-align: center;
    margin-top: 20px;
  }
  
  h3 {
    font-size: 2rem;
    margin-bottom: 15px;
  }
  
  .category-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 20px;
    max-width: 600px;
    width: 100%;
    justify-content: center;
  }
  
  .category-button {
    background: lightgrey;
    font-size: 1.2rem;
    padding: 15px;
    border: none;
    border-radius: 15px;
    cursor: pointer;
    font-weight: bold;
    width: 100%;
    height: 100%;
    transition: background 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.2);
  }
  
  .category-button:hover, .category-button:focus {
    background: linear-gradient(135deg, #ffa500, #ff6347);
    transform: translateY(-3px);
    box-shadow: 0px 6px 10px rgba(0, 0, 0, 0.3);
  }
  
  @media screen and (max-width: 768px) {
    h2 {
      font-size: 2.2rem;
    }
  
    p {
      font-size: 1.2rem;
    }
  
    .category-list {
      grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    }
  
    .category-button {
      font-size: 1rem;
      padding: 10px;
    }
  }
  </style>