<template>
  <div class="main-container">
    <Header />
    <div class="cards-container">
      <Card v-for="pokemon in pokemons" :key="pokemon.id" :pokemon="pokemon" />
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
      const response = await fetch('https://pokeapi.co/api/v2/pokemon?limit=20')
      const data = await response.json()

      const detalhes = await Promise.all(
        data.results.map(async (pokemon) => {
          const res = await fetch(pokemon.url)
          return await res.json()
        })
      )

      this.pokemons = detalhes
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
