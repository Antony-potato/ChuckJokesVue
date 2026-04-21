<script setup>
import ChuckCard from './components/ChuckCard.vue';

const chuck = [
  {
    "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
    "value": "Chuck Norris can skydive into outer space."
  },
  {
    "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
    "value": "The chief export of Chuck Norris is pain."
  },
  {
    "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
    "value": "Chuck Norris doesn't read books. He stares them down until he gets the information he wants."
  },
  {
    "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
    "value": "Time waits for no man. Unless that man is Chuck Norris."
  },
  {
    "icon_url": "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
    "value": "If you spell Chuck Norris in Scrabble, you win. Forever."
  }
];
</script>

<template>
  <div class="main-container py-5 min-vh-100">
    <header class="container text-center mb-5">
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <span class="badge bg-danger mb-2 text-uppercase tracking-wider">Actividad 12</span>
          <h1 class="display-4 fw-bold mb-3">Chuck Norris Facts</h1>
          <p class="lead text-muted">Explorando componentes de Vue y layouts responsivos con Bootstrap.</p>
          <div class="header-divider mx-auto my-4"></div>
        </div>
      </div>
    </header>

    <main class="container">
      <!-- Grid System: 3 columns on Desktop (md), 1 column on Mobile (implicit) -->
      <!-- We use justify-content-center for the last row (if it has fewer items) -->
      <div class="row row-cols-1 row-cols-md-3 g-4 justify-content-center">
        <ChuckCard
          v-for="(joke, index) in chuck"
          :key="index"
          :icon_url="joke.icon_url"
          :value="joke.value"
        />
      </div>
    </main>

    <footer class="container text-center mt-5 pt-5 text-muted border-top">
      <p>&copy; 2024 ChuckJokesVue Project | Desarrollado con Vue 3 + Vite</p>
    </footer>
  </div>
</template>

<style>
:root {
  --bg-color: #f0f2f5;
  --header-color: #1a1a1a;
}

body {
  background-color: var(--bg-color);
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  color: var(--header-color);
}

.main-container {
  background: radial-gradient(circle at top right, #ffffff, transparent),
              radial-gradient(circle at bottom left, #e9ecef, transparent);
}

.tracking-wider {
  letter-spacing: 2px;
}

.header-divider {
  width: 60px;
  height: 4px;
  background-color: #dc3545;
  border-radius: 2px;
}

.card {
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}
</style>
