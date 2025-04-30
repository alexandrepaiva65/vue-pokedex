<template>
    <header class="header">
      <h1>{{ title }}</h1>
    </header>
  </template>
  
  <script>
  export default {
    name: 'Header',
    data() {
      return {
        title: 'Vue-pokedex'
      }
    }
  }
  </script>
  
  <style scoped>
  .header {
    width: 100%;
    background-color: red;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    color: white;
    text-align: center;
  }
  
  h1 {
    margin: 0;
    font-size: 2rem;
  }
  </style>