# Base de Tecnologia do Posto Review

## Objetivo

Este documento organiza a trilha tecnica inicial para transformar o prototipo do Posto Review em um produto funcional.

## Stack Sugerida

| Camada | Sugestao | Motivo |
| --- | --- | --- |
| App mobile | React Native com Expo | Rapidez no desenvolvimento e entrega para Android/iOS |
| Backend | Node.js com Express ou Fastify | Boa produtividade para API e servicos |
| Banco de dados | PostgreSQL com PostGIS | Suporte forte para geolocalizacao |
| Autenticacao | Firebase Auth ou JWT proprio | Implementacao simples para comecar |
| Mapas | Google Maps | Boa integracao com apps mobile |
| Imagens | Firebase Storage ou AWS S3 | Upload e armazenamento escalavel |

## Estrutura Inicial Sugerida

```text
mobile/
backend/
database/
docs/
```

### Responsabilidade de Cada Parte

- `mobile/`: aplicativo mobile;
- `backend/`: API, autenticacao e regras de negocio;
- `database/`: scripts, migracoes e modelagem;
- `docs/`: documentacao complementar, wireframes e backlog.

## Modulos Principais

### Mobile

- autenticacao;
- mapa com geolocalizacao;
- tela de detalhe do posto;
- cadastro de posto;
- envio de avaliacao.

### Backend

- cadastro e login de usuarios;
- CRUD de postos;
- CRUD de avaliacoes;
- calculo de media por posto;
- moderacao basica.

### Banco de Dados

Entidades principais:

- usuarios;
- postos;
- avaliacoes;
- fotos;
- denuncias.

## Modelo de Dados Basico

### Usuario

- id
- nome
- email
- senha_hash ou provedor_auth
- data_criacao

### Posto

- id
- nome
- bandeira
- endereco
- latitude
- longitude
- criado_por
- data_criacao

### Avaliacao

- id
- usuario_id
- posto_id
- nota_geral
- nota_combustivel
- nota_atendimento
- nota_preco
- comentario
- data_criacao

## Roadmap Tecnico

### Etapa 1. Fundacao

- definir stack final;
- criar repositorio e organizacao de pastas;
- configurar ambiente do mobile e backend;
- preparar modelagem inicial do banco.

### Etapa 2. Base Funcional

- criar autenticacao;
- integrar mapa com geolocalizacao;
- listar postos proximos.

### Etapa 3. Core do Produto

- cadastrar postos;
- cadastrar avaliacoes;
- exibir media e comentarios.

### Etapa 4. Consolidacao

- upload de fotos;
- filtros e busca;
- moderacao;
- ajustes de performance.

## Requisitos Tecnicos Iniciais

Para iniciar o projeto, a base minima recomendada e:

- Node.js instalado;
- gerenciador de pacotes `npm` ou `pnpm`;
- Expo CLI ou ambiente React Native configurado;
- PostgreSQL disponivel;
- chave de API para servico de mapas.

## Proximos Passos Praticos

1. fechar a stack oficial do projeto;
2. definir as telas principais;
3. modelar o banco;
4. criar os endpoints principais;
5. iniciar o app mobile;
6. integrar mapa, autenticacao e avaliacoes.

## Observacao

Este arquivo ainda e uma base de direcionamento tecnico. Quando a implementacao comecar, ele deve crescer com:

- instrucoes de instalacao;
- comandos para rodar o projeto;
- variaveis de ambiente;
- decisoes de arquitetura;
- padrao de contribuicao.
