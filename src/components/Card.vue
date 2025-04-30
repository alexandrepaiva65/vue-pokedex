<template>
    <div class="card">
      <h3>{{ pokemon.name }}</h3>
      <h2>{{ pokemon.name }}</h2>
      <a :href="pokemon.url" target="_blank">Ver detalhes</a>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Card',
    props: {
      pokemon: {
        type: Object,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .card {
    width: 200px;
    background: #f3f3f3;
    border-radius: 8px;
    padding: 20px;
    text-align: center;
  }
  </style>
  