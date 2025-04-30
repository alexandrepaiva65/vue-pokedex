<template>
    <div class="main-container">
      <Header />
      <div class="cards-container">
        <Card v-for="pokemon in pokemons" :key="pokemon.name" :pokemon="pokemon" />
      </div>
    </div>
  </template>
  
  <script>
  import Header from '../components/Header.vue'
  import Card from '../components/Card.vue'
  
  export default {
    name: 'MainContainer',
    components: { Header, Card },
    data() {
      return {
        pokemons: []
      }
    },
    async mounted() {
        try {
            const response = await fetch('https://pokeapi.co/api/v2/pokemon')
            const data = await response.json()
            this.pokemons = data.results
        } catch (error) {
            console.error('Erro ao buscar pokemons:', error)
        }
    }

  }
  </script>
  
  <style scoped>
  .cards-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    padding: 20px;
  }
  </style>
  