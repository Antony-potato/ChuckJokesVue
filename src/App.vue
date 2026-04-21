<script setup>
const chuck = [
  {
    value: 'Chuck Norris can skydive into outer space.',
  },
  {
    value: 'The chief export of Chuck Norris is pain.',
  },
  {
    value: "Chuck Norris doesn't read books. He stares them down until he gets the information he wants.",
  },
  {
    value: 'Time waits for no man. Unless that man is Chuck Norris.',
  },
  {
    value: 'If you spell Chuck Norris in Scrabble, you win. Forever.',
  },
]
</script>

<template>
  <main class="layout">
    <section class="hero">
      <p class="eyebrow">Actividad Vue</p>
      <h1>Chuck Jokes Vue</h1>
      <p class="intro">
        Vista principal construida con Vue para mostrar chistes de Chuck Norris
        desde los datos del componente principal usando la directiva
        <code>v-for</code>.
      </p>

      <div class="hero-meta">
        <span>{{ chuck.length }} chistes cargados</span>
        <span>Vue 3 + Vite</span>
      </div>
    </section>

    <section class="panel">
      <div class="panel-head">
        <div>
          <p class="section-label">Coleccion</p>
          <h2>Listado renderizado dinamicamente</h2>
        </div>
        <p class="panel-copy">
          Cada tarjeta se genera iterando el arreglo definido en el componente
          principal.
        </p>
      </div>

      <ul class="joke-list">
        <li
          v-for="(joke, index) in chuck"
          :key="`${index}-${joke.value}`"
          class="joke-card"
        >
          <span class="joke-index">0{{ index + 1 }}</span>
          <p>{{ joke.value }}</p>
        </li>
      </ul>
    </section>
  </main>
</template>
