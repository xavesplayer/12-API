# Podcast Manager

## Descricao

O Podcast Manager e uma API para centralizar episodios de podcasts em video, organizados por categoria. O projeto permite listar episodios disponiveis e filtrar resultados pelo nome do podcast.

## Funcionalidades

- Listar episodios de podcasts por categorias, como saude, esporte, bodybuilder, mentalidade e humor.
- Filtrar episodios pelo nome do podcast.

## Endpoints

### Listar episodios

- **Metodo:** `GET`
- **Rota:** `/list`
- **Descricao:** retorna uma lista de episodios de podcasts organizados por categorias.

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
  },
  {
    "podcastName": "flow",
    "episode": "RUBENS BARRICHELLO - Flow #339",
    "videoId": "4KDGTdiOV4I",
    "cover": "https://i.ytimg.com/vi/4KDGTdiOV4I/maxresdefault.jpg",
    "link": "https://www.youtube.com/watch?v=4KDGTdiOV4I",
    "categories": ["esporte", "corrida"]
  }
]
```

### Filtrar episodios

- **Metodo:** `GET`
- **Rota:** `/episode?podcastName={nome}`
- **Descricao:** retorna episodios de podcast com base no nome informado.

Exemplo de requisicao:

```http
GET /episode?podcastName=flow
```

## Tecnologias

- TypeScript
- Node.js
- Tsup
- Tsx
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

3. Acesse os endpoints disponiveis para listar ou filtrar os episodios.

## Licenca

Uso livre para estudos e evolucao do projeto.
