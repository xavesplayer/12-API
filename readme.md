# Podcast Manager

## Descricao

O Podcast Manager e uma API em Node.js e TypeScript criada para organizar episodios de podcasts em video por categorias. A ideia do projeto e simular uma base simples de conteudos, permitindo listar todos os episodios cadastrados ou buscar episodios pelo nome do podcast.

Este e um repositorio temporario para estudos, usado por Jefferson Pereira Salvador para praticar conceitos de API sem framework, rotas, controllers, services, repositories e modelos em TypeScript.

## Funcionalidades

- Listar episodios de podcasts separados por categorias.
- Filtrar episodios pelo nome do podcast.
- Retornar respostas padronizadas em JSON.
- Organizar a aplicacao em camadas simples.

## Estrutura do Projeto

- `src/server.ts`: inicializacao do servidor.
- `src/app.ts`: configuracao principal da aplicacao.
- `src/routes`: definicao das rotas.
- `src/controllers`: entrada das requisicoes.
- `src/services`: regras de listagem e filtro.
- `src/repositories`: leitura dos dados dos podcasts.
- `src/models`: contratos usados pela aplicacao.
- `src/utils`: codigos HTTP, metodos e tipos de conteudo.

## Endpoints

### Listar episodios

- **Metodo:** `GET`
- **Rota:** `/list`
- **Descricao:** retorna a lista de episodios cadastrados.

Exemplo de resposta:

```json
[
  {
    "podcastName": "flow",
    "episode": "CBUM - Flow #319",
    "videoId": "pQSuQmUfS30",
    "cover": "https://i.ytimg.com/vi/pQSuQmUfS30/maxresdefault.jpg",
    "link": "https://www.youtube.com/watch?v=pQSuQmUfS30",
    "categories": ["saude", "esporte", "bodybuilder"]
  }
]
```

### Filtrar episodio por podcast

- **Metodo:** `GET`
- **Rota:** `/episode?podcastName={nome}`
- **Descricao:** retorna episodios de acordo com o nome do podcast informado.

Exemplo:

```http
GET /episode?podcastName=flow
```

## Tecnologias

- Node.js
- TypeScript
- Tsx
- Tsup
- @types/node

## Como executar

1. Instale as dependencias:

```bash
npm install
```

2. Inicie o servidor em modo de desenvolvimento:

```bash
npm run start:dev
```

3. Acesse os endpoints configurados no projeto.

## Autor

Jefferson Pereira Salvador

## Observacao

Repositorio temporario para estudos, testes e evolucao pessoal em desenvolvimento backend com Node.js.
