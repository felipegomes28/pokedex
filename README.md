# Pokedex

## Descrição do Projeto

Este projeto é uma Pokedex interativa desenvolvida com HTML, CSS e JavaScript puro. A aplicação consome a API pública [PokeAPI](https://pokeapi.co/) para exibir informações sobre diferentes Pokémon, incluindo seus tipos e imagens.

## Funcionalidades

- Listagem de Pokémon com paginação
- Exibição de detalhes como número, nome, tipos e imagem de cada Pokémon
- Botão "Carregar mais" para exibir mais Pokémon
- Estilização diferente para cada tipo de Pokémon

## Estrutura do Projeto

```
├── assets/
│   ├── css/
│   │   └── global.css       # Estilos globais da aplicação
│   └── js/
│       ├── main.js          # Lógica principal e manipulação do DOM
│       ├── poke-api.js      # Funções para consumo da API
│       └── pokemon-model.js # Modelo de dados para Pokémon
└── index.html              # Estrutura HTML da aplicação
```

## Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript (ES6+)
- [Normalize.css](https://necolas.github.io/normalize.css/) para normalização de estilos
- [Google Fonts](https://fonts.google.com/) (Roboto)
- [PokeAPI](https://pokeapi.co/) para obtenção dos dados dos Pokémon

## Como Funciona

1. A aplicação carrega inicialmente um conjunto limitado de Pokémon (definido pela variável `limit`)
2. Ao clicar no botão "Carregar mais", mais Pokémon são carregados da API
3. Quando o número total de Pokémon carregados se aproxima do máximo definido (`maxRecords`), o botão é removido
4. Cada Pokémon é exibido com seu número, nome, tipos e imagem
5. A cor de fundo de cada card é determinada pelo tipo principal do Pokémon

## Detalhes de Implementação

### Modelo de Dados (pokemon-model.js)

Define a classe `Pokemon` com as propriedades:
- `number`: Número do Pokémon
- `name`: Nome do Pokémon
- `type`: Tipo principal
- `types`: Array com todos os tipos
- `photo`: URL da imagem

### Consumo da API (poke-api.js)

Contém as funções:
- `getPokemons(offset, limit)`: Busca uma lista de Pokémon com paginação
- `getPokemonDetail(pokemon)`: Busca detalhes de um Pokémon específico
- `convertPokeApiDetailToPokemon(pokeDetail)`: Converte os dados da API para o modelo local

### Lógica Principal (main.js)

Responsável por:
- Inicializar a aplicação
- Carregar e exibir os Pokémon na interface
- Gerenciar o botão "Carregar mais"
- Controlar a paginação e o limite de Pokémon exibidos

## Como Executar

1. Clone ou baixe este repositório
2. Abra o arquivo `index.html` em qualquer navegador moderno
3. Não é necessário instalar dependências ou executar um servidor local

## Limitações

A aplicação está configurada para exibir um número limitado de Pokémon (definido pela variável `maxRecords` no arquivo `main.js`). Isso pode ser ajustado conforme necessário.

---

Projeto desenvolvido como parte do curso de JavaScript da Digital Innovation One (DIO).