<!-- src/App.vue -->
<template>
  <MainContainer />
</template>

<script>
import MainContainer from './containers/MainContainer.vue';
import Header from './components/Header.vue';
export default {
  name: 'App',
  components: {
    MainContainer,
  }
}
</script>

<style scoped>
/* Estilos gerais ou globais (se necessário) */
</style>
