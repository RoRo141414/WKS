<template>
  <main class="main">
    <div class="content">
      <h2>Prêt pour un Blind Test musical&nbsp;?</h2>
      <p>Affrontez vos amis et testez vos connaissances musicales sur plusieurs styles et époques.</p>
    </div>

    <section class="categories">
      <h3>Choisissez une catégorie&nbsp;:</h3>
      <div class="category-list">
        <button
          v-for="category in sortedCategories"
          :key="category"
          @click="$emit('select-category', category)"
          class="category-button"
          :aria-label="`Choisir la catégorie ${category}`"
        >
          {{ category }}
        </button>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'CategorySelector',
  data() {
    return {
      categories: ['Années 80', 'Rock', 'Pop', 'Rap', 'Variété française']
    };
  },
  computed: {
    sortedCategories() {
      return [...this.categories].sort((a, b) => a.localeCompare(b));
    }
  }
};
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  padding: 40px 20px;
  background-color: #ffffff;
  text-align: center;
  box-sizing: border-box;
  overflow: hidden;
}

.content {
  max-width: 700px;
  width: 100%;
  margin-bottom: 40px;
  color: #222;
}

h2 {
  font-size: 3.2rem;
  font-weight: 700;
  margin-bottom: 20px;
  color: #333;
}

p {
  font-size: 1.6rem;
  line-height: 1.6;
  color: #555;
}

.categories {
  width: 100%;
  margin-top: 30px;
}

h3 {
  font-size: 2.2rem;
  margin-bottom: 20px;
  color: #333;
}

.category-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 20px;
  max-width: 700px;
  width: 100%;
}

.category-button {
  background-color: #f7f7f7;
  color: #333;
  font-size: 1.2rem;
  font-weight: 600;
  padding: 15px 10px;
  border: none;
  border-radius: 12px;
  cursor: pointer;
  width: 100%;
  transition: background 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.category-button:hover,
.category-button:focus {
  background: linear-gradient(135deg, #ff416c, #00dbde);
  color: #fff;
  transform: translateY(-4px);
  box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
  outline: none;
}

@media (max-width: 768px) {
  h2 {
    font-size: 2.4rem;
  }

  p {
    font-size: 1.3rem;
  }

  h3 {
    font-size: 1.8rem;
  }

  .category-list {
    grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  }

  .category-button {
    font-size: 1rem;
    padding: 12px 8px;
  }
}
</style>