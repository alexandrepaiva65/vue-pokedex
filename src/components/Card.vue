<template>
  <div class="card">
    <img :src="pokemon.sprites.front_default" :alt="pokemon.name" />
    <h3>{{ pokemon.name.toUpperCase() }}</h3>
    <p>
      Tipo:
      <span v-for="(tipo, index) in pokemon.types" :key="tipo.type.name">
        {{ tipo.type.name }}<span v-if="index < pokemon.types.length - 1">, </span>
      </span>
    </p>
    <a :href="`https://pokeapi.co/api/v2/pokemon/${pokemon.id}`" target="_blank">Ver detalhes</a>
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
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
}
.card img {
  width: 100px;
  height: 100px;
  object-fit: contain;
}
.card p {
  margin: 10px 0;
  font-weight: bold;
}
</style>
