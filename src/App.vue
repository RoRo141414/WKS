<script setup>
import HelloWorld from './components/HelloWorld.vue';
import TheWelcome from './components/TheWelcome.vue';
import HeaderComponent from './components/header.vue';
import template from './components/main.vue';
import FooterComponent from './components/footer.vue';
</script>

<template>
  <HeaderComponent />

  <main>
    <MainComponent />
  </main>

  <FooterComponent />
</template>

<style scoped>
header {
  line-height: 1.5;
  text-align: center;
  padding: 1rem;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  max-width: 150px;
  height: auto;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-right: calc(var(--section-gap, 2rem) / 2);
    text-align: left;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 1rem;
  }
}
</style>