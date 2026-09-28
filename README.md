# Vue Pokédex

Projeto simples de estudo desenvolvido para praticar os fundamentos do Vue 3 com Vite e o consumo de uma API externa.

A aplicação consulta a [PokéAPI](https://pokeapi.co/) e exibe uma lista de 20 Pokémon. Para cada item, são carregados os detalhes do Pokémon, como nome, imagem, tipos e link para a resposta correspondente da API.

## Objetivos de estudo

- Criar componentes reutilizáveis com Vue 3;
- Trabalhar com propriedades (`props`) e renderização de listas;
- Buscar dados externos com `fetch` e `async/await`;
- Combinar requisições com `Promise.all`;
- Organizar a aplicação em componentes e containers;
- Desenvolver e gerar uma aplicação Vue usando Vite.

## Tecnologias

- [Vue 3](https://vuejs.org/)
- [Vite](https://vite.dev/)
- [PokéAPI](https://pokeapi.co/)

## Como executar

### Pré-requisitos

- Node.js instalado;
- npm instalado.

### Instalação

```sh
npm install
```

### Ambiente de desenvolvimento

Inicie o servidor local com:

```sh
npm run dev
```

O Vite exibirá no terminal o endereço para acessar a aplicação no navegador.

### Build de produção

Para gerar os arquivos otimizados:

```sh
npm run build
```

Para visualizar o build localmente:

```sh
npm run preview
```

## Estrutura principal

- `src/App.vue`: componente raiz da aplicação;
- `src/containers/MainContainer.vue`: busca os dados da PokéAPI e organiza os cards;
- `src/components/Header.vue`: cabeçalho da aplicação;
- `src/components/Card.vue`: apresenta os dados de cada Pokémon;
- `src/assets/base.css`: estilos base.
